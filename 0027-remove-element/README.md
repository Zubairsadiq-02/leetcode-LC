<h3>SOLUTION</h3>
<h2>Aproach used :</h2>
<p>BRUTE FORCE </p> <br> <p>TWO POINTERS</p> 
<p>
Two pointers are taken in which <bold>I</bold> scans the array
<bold>K</bold> stores the next valid element.
  <p>
     for (int i = 0;i < n ; i++){
            if(nums[i] != val ){
                nums[k] = nums[i];
                k++;
                        </p>
Time  → O(n)
Space → O(1)</p>
</p> <br> <img width="900" height="200" alt="LC-27 1" src="https://github.com/user-attachments/assets/bf8eb776-3dd5-437d-ad04-60547b22069c" />

<br>
<img width="800" height="600" alt="LC-27 2" src="https://github.com/user-attachments/assets/d92cc09d-5eb2-4e05-b64e-cd5ae4907184" />



