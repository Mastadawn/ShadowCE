
--[[
AztupBrew(Fork of IronBrew2): obfuscation; Version 2.7.2
]]
return(function(V2_i,V2_a,V2_a)local V2_k=string.char;local V2_e=string.sub;local V2_n=table.concat;local V2_o=math.ldexp;local V2_p=getfenv or function()return _ENV end;local V2_l=select;local V2_g=unpack or table.unpack;local V2_j=tonumber;local function V2_m(V2_h)local V2_b,V2_c,V2_d="","",{}local V2_f=256;local V2_g={}for V2_a=0,V2_f-1 do V2_g[V2_a]=V2_k(V2_a)end;local V2_a=1;local function V2_i()local V2_b=V2_j(V2_e(V2_h,V2_a,V2_a),36)V2_a=V2_a+1;local V2_c=V2_j(V2_e(V2_h,V2_a,V2_a+V2_b-1),36)V2_a=V2_a+V2_b;return V2_c end;V2_b=V2_k(V2_i())V2_d[1]=V2_b;while V2_a<#V2_h do local V2_a=V2_i()if V2_g[V2_a]then V2_c=V2_g[V2_a]else V2_c=V2_b..V2_e(V2_b,1,1)end;V2_g[V2_f]=V2_b..V2_e(V2_c,1,1)V2_d[#V2_d+1],V2_b,V2_f=V2_c,V2_c,V2_f+1 end;return table.concat(V2_d)end;local V2_j=V2_m('23E23I27523H23827523I1I1H1V1Q1D1A1C1N1G1P23H2742751P1V1J1R23H23D27921I1A1A1E21L1R1A23H22N2791M27W1E1D21W2292291E1V27F1R1S27I2281T1H1J2291C1V192291M225192241E1E22421F23A27923023B27923J29027529423G27922M29623I29423H23I23027623I27M27929C23I29E29K29O29829O29429429R29O279');local V2_a=(bit or bit32);local V2_d=V2_a and V2_a.bxor or function(V2_a,V2_b)local V2_c,V2_d,V2_e=1,0,10 while V2_a>0 and V2_b>0 do local V2_e,V2_f=V2_a%2,V2_b%2 if V2_e~=V2_f then V2_d=V2_d+V2_c end V2_a,V2_b,V2_c=(V2_a-V2_e)/2,(V2_b-V2_f)/2,V2_c*2 end if V2_a<V2_b then V2_a=V2_b end while V2_a>0 do local V2_b=V2_a%2 if V2_b>0 then V2_d=V2_d+V2_c end V2_a,V2_c=(V2_a-V2_b)/2,V2_c*2 end return V2_d end local function V2_c(V2_b,V2_a,V2_c)if V2_c then local V2_a=(V2_b/2^(V2_a-1))%2^((V2_c-1)-(V2_a-1)+1);return V2_a-V2_a%1;else local V2_a=2^(V2_a-1);return(V2_b%(V2_a+V2_a)>=V2_a)and 1 or 0;end;end;local V2_a=1;local function V2_b()local V2_e,V2_b,V2_f,V2_c=V2_i(V2_j,V2_a,V2_a+3);V2_e=V2_d(V2_e,126)V2_b=V2_d(V2_b,126)V2_f=V2_d(V2_f,126)V2_c=V2_d(V2_c,126)V2_a=V2_a+4;return(V2_c*16777216)+(V2_f*65536)+(V2_b*256)+V2_e;end;local function V2_h()local V2_b=V2_d(V2_i(V2_j,V2_a,V2_a),126);V2_a=V2_a+1;return V2_b;end;local function V2_f()local V2_c,V2_b=V2_i(V2_j,V2_a,V2_a+2);V2_c=V2_d(V2_c,126)V2_b=V2_d(V2_b,126)V2_a=V2_a+2;return(V2_b*256)+V2_c;end;local function V2_m()local V2_d=V2_b();local V2_a=V2_b();local V2_e=1;local V2_d=(V2_c(V2_a,1,20)*(2^32))+V2_d;local V2_b=V2_c(V2_a,21,31);local V2_a=((-1)^V2_c(V2_a,32));if(V2_b==0)then if(V2_d==0)then return V2_a*0;else V2_b=1;V2_e=0;end;elseif(V2_b==2047)then return(V2_d==0)and(V2_a*(1/0))or(V2_a*(0/0));end;return V2_o(V2_a,V2_b-1023)*(V2_e+(V2_d/(2^52)));end;local V2_o=V2_b;local function V2_q(V2_b)local V2_c;if(not V2_b)then V2_b=V2_o();if(V2_b==0)then return'';end;end;V2_c=V2_e(V2_j,V2_a,V2_a+V2_b-1);V2_a=V2_a+V2_b;local V2_b={}for V2_a=1,#V2_c do V2_b[V2_a]=V2_k(V2_d(V2_i(V2_e(V2_c,V2_a,V2_a)),126))end return V2_n(V2_b);end;local V2_a=V2_b;local function V2_o(...)return{...},V2_l('#',...)end local function V2_k()local V2_j={};local V2_i={};local V2_a={};local V2_l={[#{"1 + 1 = 111";"1 + 1 = 111";}]=V2_i,[#{{546;92;586;16};"1 + 1 = 111";{241;722;29;769};}]=nil,[#{"1 + 1 = 111";{56;505;249;443};{505;930;434;211};{896;690;657;9};}]=V2_a,[#{{758;941;63;255};}]=V2_j,};local V2_a=V2_b()local V2_e={}for V2_c=1,V2_a do local V2_b=V2_h();local V2_a;if(V2_b==2)then V2_a=(V2_h()~=0);elseif(V2_b==0)then V2_a=V2_m();elseif(V2_b==3)then V2_a=V2_q();end;V2_e[V2_c]=V2_a;end;for V2_i=1,V2_b()do local V2_a=V2_h();if(V2_c(V2_a,1,1)==0)then local V2_d=V2_c(V2_a,2,3);local V2_g=V2_c(V2_a,4,6);local V2_a={V2_f(),V2_f(),nil,nil};if(V2_d==0)then V2_a[3]=V2_f();V2_a[4]=V2_f();elseif(V2_d==1)then V2_a[3]=V2_b();elseif(V2_d==2)then V2_a[3]=V2_b()-(2^16)elseif(V2_d==3)then V2_a[3]=V2_b()-(2^16)V2_a[4]=V2_f();end;if(V2_c(V2_g,1,1)==1)then V2_a[2]=V2_e[V2_a[2]]end if(V2_c(V2_g,2,2)==1)then V2_a[3]=V2_e[V2_a[3]]end if(V2_c(V2_g,3,3)==1)then V2_a[4]=V2_e[V2_a[4]]end V2_j[V2_i]=V2_a;end end;for V2_a=1,V2_b()do V2_i[V2_a-1]=V2_k();end;V2_l[3]=V2_h();return V2_l;end;local function V2_n(V2_a,V2_b,V2_i)V2_a=(V2_a==true and V2_k())or V2_a;return(function(...)local V2_f=V2_a[1];local V2_d=V2_a[3];local V2_a=V2_a[2];local V2_j=V2_o local V2_c=1;local V2_e=-1;local V2_m={};local V2_k={...};local V2_h=V2_l('#',...)-1;local V2_a={};local V2_b={};for V2_a=0,V2_h do if(V2_a>=V2_d)then V2_m[V2_a-V2_d]=V2_k[V2_a+1];else V2_b[V2_a]=V2_k[V2_a+#{"1 + 1 = 111";}];end;end;local V2_a=V2_h-V2_d+1 local V2_a;local V2_d;while true do V2_a=V2_f[V2_c];V2_d=V2_a[1];if V2_d<=6 then if V2_d<=2 then if V2_d<=0 then local V2_c=V2_a[2]local V2_d,V2_a=V2_j(V2_b[V2_c](V2_g(V2_b,V2_c+1,V2_a[3])))V2_e=V2_a+V2_c-1 local V2_a=0;for V2_c=V2_c,V2_e do V2_a=V2_a+1;V2_b[V2_c]=V2_d[V2_a];end;elseif V2_d>1 then local V2_d=V2_a[2];local V2_c=V2_b[V2_a[3]];V2_b[V2_d+1]=V2_c;V2_b[V2_d]=V2_c[V2_a[4]];else local V2_a=V2_a[2]V2_b[V2_a]=V2_b[V2_a](V2_g(V2_b,V2_a+1,V2_e))end;elseif V2_d<=4 then if V2_d>3 then local V2_c=V2_a[2];local V2_d=V2_b[V2_a[3]];V2_b[V2_c+1]=V2_d;V2_b[V2_c]=V2_d[V2_a[4]];else V2_b[V2_a[2]]=V2_a[3];end;elseif V2_d>5 then V2_b[V2_a[2]]();else V2_b[V2_a[2]]=V2_i[V2_a[3]];end;elseif V2_d<=10 then if V2_d<=8 then if V2_d==7 then V2_b[V2_a[2]]=V2_i[V2_a[3]];else do return end;end;elseif V2_d>9 then V2_b[V2_a[2]]();else local V2_h;local V2_m,V2_l;local V2_k;local V2_d;V2_b[V2_a[2]]=V2_i[V2_a[3]];V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_b[V2_a[2]]=V2_i[V2_a[3]];V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_d=V2_a[2];V2_k=V2_b[V2_a[3]];V2_b[V2_d+1]=V2_k;V2_b[V2_d]=V2_k[V2_a[4]];V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_b[V2_a[2]]=V2_a[3];V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_d=V2_a[2]V2_m,V2_l=V2_j(V2_b[V2_d](V2_g(V2_b,V2_d+1,V2_a[3])))V2_e=V2_l+V2_d-1 V2_h=0;for V2_a=V2_d,V2_e do V2_h=V2_h+1;V2_b[V2_a]=V2_m[V2_h];end;V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_d=V2_a[2]V2_b[V2_d]=V2_b[V2_d](V2_g(V2_b,V2_d+1,V2_e))V2_c=V2_c+1;V2_a=V2_f[V2_c];V2_b[V2_a[2]]();V2_c=V2_c+1;V2_a=V2_f[V2_c];do return end;end;elseif V2_d<=12 then if V2_d==11 then do return end;else local V2_a=V2_a[2]V2_b[V2_a]=V2_b[V2_a](V2_g(V2_b,V2_a+1,V2_e))end;elseif V2_d==13 then local V2_c=V2_a[2]local V2_d,V2_a=V2_j(V2_b[V2_c](V2_g(V2_b,V2_c+1,V2_a[3])))V2_e=V2_a+V2_c-1 local V2_a=0;for V2_c=V2_c,V2_e do V2_a=V2_a+1;V2_b[V2_c]=V2_d[V2_a];end;else V2_b[V2_a[2]]=V2_a[3];end;V2_c=V2_c+1;end;end);end;return V2_n(true,{},V2_p())();end)(string.byte,table.insert,setmetatable);
