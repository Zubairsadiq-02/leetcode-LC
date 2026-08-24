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
                        <p>This  is the very important logic here Two Pointers ka basic idea

Is problem mein humare paas do pointers hain:

i → array ko check karta hai
k → valid elements ko store karta hai

Socho i ek scanner hai aur k ek collector.

i kya karta hai?

i array ke har element ko one-by-one dekhta hai.

[3, 2, 2, 3]
 ↑
 i

Phir:

3 → remove
2 → keep
2 → keep
3 → remove

i ka kaam bas ye decide karna hai:

"Ye element rakhna hai ya nahi?"

k kya karta hai?

k decide karta hai ki jo element rakhna hai, usko array ke starting part mein kahan rakhna hai.

Starting:

k = 0

Jab i ko valid element milta hai:

nums[k] = nums[i];

Matlab:

"Is valid element ko k wali position par rakh do."

Uske baad:

k++;

Matlab:

"Ye position fill ho gayi. Ab next valid element ko next position par rakhenge."

Example
nums = [3, 2, 2, 3]
val = 3

Initially:

i = 0
k = 0
i = 0
nums[i] = 3

3 ko remove karna hai.

So kuch nahi karenge.

i → next
k → same
i = 1
nums[i] = 2

2 ko rakhna hai.

k = 0, so:

nums[0] = nums[1];

Array:

[2, 2, 2, 3]
 ↑  ↑
 k  i

Then:

k++

Now:

k = 1
i = 2

Again 2 valid hai.

nums[1] = nums[2];

Then:

k++;

Now:

k = 2
i = 3
nums[i] = 3

3 ko remove karna hai.

So kuch nahi karenge.

Finally:

k = 2

Return 2.

First 2 positions:

[2, 2]
Why is this called "Two Pointers"?

Because hum same array par do positions track kar rahe hain:

i → reads/checks elements
k → writes/stores valid elements

They don't necessarily move together.

For example:

i = 0, k = 0
i = 1, k = 0
i = 2, k = 1
i = 3, k = 2

Notice:

i har iteration mein aage badhta hai.

k sirf tab aage badhta hai jab valid element milta hai.

The main intuition 🧠

Brute force mein hum bol rahe the:

"Element delete mila → baaki sabko shift karo."

Two-pointer mein hum bolte hain:

"Delete karne ki zarurat hi nahi. Jo elements chahiye, unko directly front mein copy karte jao."

That's why:

i → Find
k → Place

Aur isi wajah se brute force ka O(n²) improve hokar:

Time  → O(n)
Space → O(1)</p>
</p> <br> <img width="900" height="200" alt="LC-27 1" src="https://github.com/user-attachments/assets/bf8eb776-3dd5-437d-ad04-60547b22069c" />

<br>
<img width="800" height="600" alt="LC-27 2" src="https://github.com/user-attachments/assets/d92cc09d-5eb2-4e05-b64e-cd5ae4907184" />



