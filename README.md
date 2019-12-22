using System.Collections;
using UnityEngine;
using UnityEngine.UI;

public class Hud : MonoBehaviour
{
    public Sprite[] HeartSprites;

    public Image HeartUI;

    private static PlayerAL player1;

    private void Start()
    {
        player1 = GameObject.FindGameObjectWithTag("Player").GetComponent<PlayerAL>();
    }

    private void Update()
    {
        HeartUI.sprite = HeartSprites[PlayerAL.currHealth];
    }
}
