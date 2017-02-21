# homeWork
using UnityEngine;
using System.Collections;

public class basic_conditional : MonoBehaviour {

	public bool goToWork;
	public GameObject mover;


	// Use this for initialization
	void Start () {
	
	}
	
	// Update is called once per frame
	void Update () {
		Debug.Log ("game object is at ... " + mover.transform.position);
		if (Input.GetKeyDown ("left")) {
			mover.transform.position += new Vector3 (0, 0, -10);
		}		if (Input.GetKeyDown ("right")) {
			mover.transform.position += new Vector3 (0, 0, 10);
		}		if (Input.GetKeyDown ("up")) {
			mover.transform.position += new Vector3 (-10, 0, 0);
		}		if (Input.GetKeyDown ("down")) {
			mover.transform.position += new Vector3 (10, 0, 0);
		}
		//outer orbs
		if (mover.transform.position == new Vector3 (30, 2, 0)) {
			mover.transform.position += new Vector3 (40, 0, 30);
			}			if (mover.transform.position == new Vector3 (0, 2, 30)) {
			mover.transform.position += new Vector3 (80, 0, -40);
			}		if (mover.transform.position == new Vector3 (-30, 2, 0)) {
			mover.transform.position += new Vector3 (-40, 0, 90);
			}	if (mover.transform.position == new Vector3 (0, 2, -30)) {
			mover.transform.position += new Vector3 (50, 0, -40);
			}
		//inner orbs
if (mover.transform.position == new Vector3 (10, 2, 10)) {
	mover.transform.position += new Vector3 (-40, 0, 60);
	}
	if (mover.transform.position == new Vector3 (10, 2, -10)) {
		mover.transform.position += new Vector3 (-60, 0, 40);
		}
	if (mover.transform.position == new Vector3 (-10, 2, 10)) {
		mover.transform.position += new Vector3 (-40, 0, 30);
		}
		if (mover.transform.position == new Vector3 (-10, 2, -10)) {
			mover.transform.position += new Vector3 (-20, 0, -40);
		}

		//outer walls closer to orbs
		if (mover.transform.position == new Vector3 (-50, 2, 20)) {
			mover.transform.position += new Vector3 (-50, 0, 10);
			}
		if (mover.transform.position == new Vector3 (50, 2, -20)) {
			mover.transform.position += new Vector3 (50, 0, -10);
			}
		if (mover.transform.position == new Vector3 (-50, 2, -20)) {
			mover.transform.position += new Vector3 (-50, 0, -10);
			}
		if (mover.transform.position == new Vector3 (50, 2, 20)) {
			mover.transform.position += new Vector3 (50, 0, 10);
			}
		// outher wall long wall
		if (mover.transform.position == new Vector3 (-30, 2, 50)) {
			mover.transform.position += new Vector3 (-20, 0, 40);
		}
		if (mover.transform.position == new Vector3 (30, 2, -50)) {
			mover.transform.position += new Vector3 (20, 0, -40);
		}
		if (mover.transform.position == new Vector3 (-30, 2, -50)) {
			mover.transform.position += new Vector3 (-20, 0, -40);
		}
		if (mover.transform.position == new Vector3 (30, 2, 50)) {
			mover.transform.position += new Vector3 (20, 0, 40);

		}
		//inner wall
		if (mover.transform.position == new Vector3 (-30, 2, 50)) {
			mover.transform.position += new Vector3 (-20, 0, 40);
		}
		if (mover.transform.position == new Vector3 (30, 2, -50)) {
			mover.transform.position += new Vector3 (20, 0, -40);
		}
		if (mover.transform.position == new Vector3 (-30, 2, -50)) {
			mover.transform.position += new Vector3 (-20, 0, -40);
		}
		if (mover.transform.position == new Vector3 (30, 2, 50)) {
			mover.transform.position += new Vector3 (20, 0, 40);

		}
		//blockers
		if (mover.transform.position == new Vector3 (-15, 2, 0)) {
			mover.transform.position += new Vector3 (-20, 0, 40);
		}
		if (mover.transform.position == new Vector3 (15, 2, 0)) {
			mover.transform.position += new Vector3 (20, 0, -40);
		}

	}
}

