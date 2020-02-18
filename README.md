# 阴阳历日期转换比较以及节假日判断和获取

示例:判断是否传统节假日
````php
    var_dump((new Lunar)->getFestival(2020, 01, 25));
    // OUTPUT
   /** array(4) {
      ["is"]=>
      bool(true)
      ["type"]=>
      int(0)
      ["info"]=>
      string(6) "春节"
      ["wish"]=>
      string(48) "春回大地风光好，福满人间喜事多。"
    }
    **/
````

* **public function convertSolarToLunar($year, $month, $date)**\
将阳历转换为阴历\
@param year 公历-年\
@param month 公历-月\
@param date 公历-日
     
* **public function convertLunarToSolar($year, $month, $date)**\     
将阴历转换为阳历\
@param year 阴历-年\
@param month 阴历-月，闰月处理：例如如果当年闰五月，那么第二个五月就传六月，相当于阴历有13个月，只是有的时候第13个月的天数为0\
@param date 阴历-日

* **public function convertLunarToSolar($year, $month, $date)**\
将阴历转换为阳历\
@param year 阴历-年\
@param month 阴历-月，闰月处理：例如如果当年闰五月，那么第二个五月就传六月，相当于阴历有13个月，只是有的时候第13个月的天数为0\
@param date 阴历-日
 
* **public function isLeapYear($year)**\
判断是否是闰年\
@param year

* **public function getLunarYearName($year)**\
获取干支纪年\
@param year

* **public function getYearZodiac($year)**\
根据阴历年获取生肖\
@param year 阴历年

* **public function getSolarMonthDays($year, $month)**\ 
获取阳历月份的天数\
@param year 阳历-年\
@param month 阳历-月

* **public function getLunarMonthDays($year, $month)**\
获取阴历月份的天数\
@param year 阴历-年\
@param month 阴历-月，从一月开始
 
* **public function getLunarMonths($year)**\
获取阴历每月的天数的数组\
@param year
 
* **public function getLunarYearDays($year)** \
获取农历某年的天数\
@param year 农历年份

* **public function getLunarYearMonths($year)**\
获取农历某年的月数\
@param year 农历年份   

* **public function getLeapMonth($year)**\
获取闰月\
@param year 阴历年份

* **public function getDaysBetweenLunar($year, $month, $date)**\
计算阴历日期与正月初一相隔的天数\
@param year\
@param month\
@param date

* **public function getDaysBetweenSolar($year, $cmonth, $cdate, $dmonth, $ddate)**\
计算2个阳历日期之间的天数\
@param year 阳历年\
@param cmonth\
@param cdate\
@param dmonth 阴历正月对应的阳历月份\
@param ddate 阴历初一对应的阳历天数

* **public function getLunarByBetween($year, $between)**\
根据距离正月初一的天数计算阴历日期\
@param year 阳历年\
@param between 天数
 
* **public function getCapitalNum($num, $isMonth)**\
获取数字的阴历叫法\
@param num 数字\
@param isMonth 是否是月份的数字

* **public function getFestival($year, $month, $day)**\
判断是否传统节假日
````php
    var_dump((new Lunar)->getFestival(2020, 01, 25));
    // OUTPUT
   /** array(4) {
      ["is"]=>
      bool(true)
      ["type"]=>
      int(0)
      ["info"]=>
      string(6) "春节"
      ["wish"]=>
      string(48) "春回大地风光好，福满人间喜事多。"
    }
    **/
````
 
