"# Field-Programmable-Gate-Array-Design"  
**Hardware Architecture** about **Elliptic Curve Cryptography**  
**◼ Submodule**  
**◆ Controller**  
![image](https://github.com/RayChao1030/Field-Programmable-Gate-Array-Design/assets/76627328/08bfca5e-9415-4309-80c4-93123126b23e)  

**◆ ALU**  
![image](https://github.com/RayChao1030/Field-Programmable-Gate-Array-Design/assets/76627328/12f8cfe4-663d-47a3-9939-51f2ba648075)  

**◼ Top module**  
![image](https://github.com/RayChao1030/Field-Programmable-Gate-Array-Design/assets/76627328/27c2f5eb-4ee7-4d9a-ab96-c1fd45f5343f)  
**Hardware Design**  
**the Modulus operation** (referred to as **Mod**)   
Utilized long division, starting from the MSB and comparing it with a value P over 64 bits. If the taken-out partial remainder is larger, subtraction is performed; otherwise, it is not needed. After storing back the partial remainder, it is left-shifted by one bit. By cascading the aforementioned operations in a dual-extreme manner, we can halve the number of cycles needed for one mod p operation.  
![image](https://github.com/RayChao1030/Field-Programmable-Gate-Array-Design/assets/76627328/95d8f624-82ff-4d56-8ec5-967b52c8803b)  
**The Mul64*64 operation**   
Involved multiplying two 64-bit inputs by breaking them down into 16-bit by 16-bit multiplications. Each cycle multiplies a 16-bit multiplicand with the 64-bit multiplier to accumulate partial products. Within 4 cycles, the multiplication of two 64-bit numbers can be completed.
![image](https://github.com/RayChao1030/Field-Programmable-Gate-Array-Design/assets/76627328/d83e9fcc-e94e-47de-8ba7-b8fd51b25593)  
**The Inv_mod operation**  
Utilized Fermat's Little Theorem to find the inverse modulo p, By exploiting the properties of modular exponentiation, iterated through the exponent bits of a, raising a to powers of two and accumulating the product, thus completing the calculation.MORE UPDATED SOON

