# Redirecting the scene
## Aim:
To Redirecting the scene in the unity engine.


## Algorithm:
### Step 1:

Open the unity engine.

### Step 2:

Create a new plane and create a cube and give color for the cube.

### Step 3:

Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:

Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:

Create the C# script file in the Assets and write the Coding for the Redirecting.

### Step 6:

Next Create a another new scene named as page2.

### Step 7:

In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

### Step 8:

Click the Build and run button in the Build settings and run the scene.

### Step 9:

The Sphere after touching the cube it will disappeared and Press the key [space] for redircting to the new scene that is page2.



## Program:
Developed By: **Akash A**
</br>
Register No.: **212221230003**
```python
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class PlayerController : MonoBehaviour
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
        if (Input.GetKeyDown(KeyCode.Space))
        {
            SceneManager.LoadScene("level2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "cube")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Output:
![image](https://github.com/Akash020803/Redirecting-the-scene/assets/94177474/2b859dfb-e1f5-4d6b-8872-dcc1c70c2f1a)

### After the Ball hit the cube:
![image](https://github.com/Akash020803/Redirecting-the-scene/assets/94177474/11d1db80-5ed1-427b-af1d-2e9f1fa50dfc)
### Redirected scene:
![image](https://github.com/Akash020803/Redirecting-the-scene/assets/94177474/b0c0aa52-8dc5-4e1a-933c-610e6b713669)



## Result:
Thus the above C# coding is successfully redirecting the scene in the unity engine.
