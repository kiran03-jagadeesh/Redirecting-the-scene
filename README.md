# Redirecting-the-scene

## Aim:
To redirect a scene using C# program in Unity engine.



## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new plane and create a cube and give color for the cube.

Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the scene1 after hit the sphere to cube.

Step 6:
Next Create a another new scene named as scene1.

Step 7:
In File->Build settings and drop the both first scene and scene1 scene in the Scenes in build setting.

Step 8:
Click the Build and run button in the Build settings and run the scene.

Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is scene1.

## Program:
~~~
Developed By: kiran J
Register Number: 212221240022
~~~
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine.SceneManagement;
using UnityEngine;

public class objectone1 : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("exp71");
        }
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "square")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
~~~

## Output:
![Exp7-1](https://github.com/kiran03-jagadeesh/Redirecting-the-scene/assets/94174536/470f9095-5abf-432a-a713-4614f1d87e9c)
![Exp7-2](https://github.com/kiran03-jagadeesh/Redirecting-the-scene/assets/94174536/1b2f33f3-1e2f-479a-a7a9-58102c6fb227)
![Exp7-3](https://github.com/kiran03-jagadeesh/Redirecting-the-scene/assets/94174536/f41d8a40-fe6b-493c-8c2f-9fb51427d394)

## Result:
Thus, a scene is redirected in Unity engine using a C# program.

