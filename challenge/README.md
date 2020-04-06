# Bootcamp: UCB-VIRT-DATA-PT-03-2020-U-B-TTH
### Bootcamp Challenge #4 - 4/5/2020
Bootcamp Challenge 4: Module PyCitySchools with Pandas

### Datasets Used
- [Schools Complete](https://courses.bootcampspot.com/courses/140/files/35407)
- [Students Complete](https://courses.bootcampspot.com/courses/140/files/35405)

### Jupyter Notebook Created
- [PyCitySchools_Challenge](PyCitySchools_Challenge.ipynb)
- [Results](output/results.txt)

### Challenge Description
The grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent of this academic dishonesty, they want to uphold the standards of state testing and have turned to you for help.

After assessing the situation with the school superintendent and Maria, you decide the best approach is to:
- Replace the ninth-grade math and reading scores from Thomas High School.
- Keep all other data associated with the ninth-grade students and Thomas High School intact.

The goals of this challenge are for you to:
- Filter DataFrames using logical operators.
- Replace the incorrect values with NaN.
- Explain how your PyCitySchools analysis changes after you handle the incorrect data.  

### Challenge Observations
The following categories below summarize the overall impact to each of the categories as outlined in the challenge. To consider the impact, the data was first captured in the "As-Is" state. Then the script was run again after putting NaN values for the 9th graders in Thomas High School, the data was revisited, and the following categories analyzed. This corresponds to Part 5 of the challenge.

#### District Summary Impact
As the entire district contains many schools and students, it is to be expected that any impact originating from the 9th Grade Thomas High School will be averaged out and thus we should not expect to see drastic changes across the district.

In the original dataset where we included Thomas High School 9th grade, we observed the following statistics.

**Original**
Average Math Score: 79.0
Average Reading Score %: 81.9
Passing Math %: 74.98
Passing Reading	%: 85.81
Overall Passing: 65.17

When the scripts were updated to replace the Math and Reading scores with NaN for all students attending 9th grade Thomas High School we observed the following statistics.

**NaN Modified**
Average Math Score: 78.9
Average Reading Score	%: 81.9
Passing Math	%: 73.88
Passing Reading	%: 84.65
Overall Passing: 64.09

The difference observed by replacing the 9th grade Thomas High School math and reading scores to NaN resulted in, district wide, a drop of .1% on the average Math Score, 0% change in the Average Reading Score, Passing Math % dropped 1.1%, Passing Reading % Dropped 1.16%, and overall passing dropped 1.08%. 
			
#### School Impact
Logically there was no impact to any school (individually) other than Thomas High School. Included here are the 2 sets of data that breaks down the statistics across all schools. We observe that only the Thomas High School row has data fields that have changed from the challenge assignment. As expected, changing the reading and math scores for Thomas HS did not impact the number of schools, the names of the schools, the type of school, their budgets, nor the number of students per school.

**Original**
	School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Bailey High School	District	4976	$3,124,928.00	$628.00	77.048432	81.033963	66.680064	81.933280	54.642283
Cabrera High School	Charter	1858	$1,081,356.00	$582.00	83.061895	83.975780	94.133477	97.039828	91.334769
Figueroa High School	District	2949	$1,884,411.00	$639.00	76.711767	81.158020	65.988471	80.739234	53.204476
Ford High School	District	2739	$1,763,916.00	$644.00	77.102592	80.746258	68.309602	79.299014	54.289887
Griffin High School	Charter	1468	$917,500.00	$625.00	83.351499	83.816757	93.392371	97.138965	90.599455
Hernandez High School	District	4635	$3,022,020.00	$652.00	77.289752	80.934412	66.752967	80.862999	53.527508
Holden High School	Charter	427	$248,087.00	$581.00	83.803279	83.814988	92.505855	96.252927	89.227166
Huang High School	District	2917	$1,910,635.00	$655.00	76.629414	81.182722	65.683922	81.316421	53.513884
Johnson High School	District	4761	$3,094,650.00	$650.00	77.072464	80.966394	66.057551	81.222432	53.539172
Pena High School	Charter	962	$585,858.00	$609.00	83.839917	84.044699	94.594595	95.945946	90.540541
Rodriguez High School	District	3999	$2,547,363.00	$637.00	76.842711	80.744686	66.366592	80.220055	52.988247
Shelton High School	Charter	1761	$1,056,600.00	$600.00	83.359455	83.725724	93.867121	95.854628	89.892107
Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.418349	83.848930	93.272171	97.308869	90.948012
Wilson High School	Charter	2283	$1,319,574.00	$578.00	83.274201	83.989488	93.867718	96.539641	90.582567
Wright High School	Charter	1800	$1,049,400.00	$583.00	83.682222	83.955000	93.333333	96.611111	90.333333

**NaN Modified**
School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Bailey High School	District	4976	$3,124,928.00	$628.00	77.048432	81.033963	66.680064	81.933280	54.642283
Cabrera High School	Charter	1858	$1,081,356.00	$582.00	83.061895	83.975780	94.133477	97.039828	91.334769
Figueroa High School	District	2949	$1,884,411.00	$639.00	76.711767	81.158020	65.988471	80.739234	53.204476
Ford High School	District	2739	$1,763,916.00	$644.00	77.102592	80.746258	68.309602	79.299014	54.289887
Griffin High School	Charter	1468	$917,500.00	$625.00	83.351499	83.816757	93.392371	97.138965	90.599455
Hernandez High School	District	4635	$3,022,020.00	$652.00	77.289752	80.934412	66.752967	80.862999	53.527508
Holden High School	Charter	427	$248,087.00	$581.00	83.803279	83.814988	92.505855	96.252927	89.227166
Huang High School	District	2917	$1,910,635.00	$655.00	76.629414	81.182722	65.683922	81.316421	53.513884
Johnson High School	District	4761	$3,094,650.00	$650.00	77.072464	80.966394	66.057551	81.222432	53.539172
Pena High School	Charter	962	$585,858.00	$609.00	83.839917	84.044699	94.594595	95.945946	90.540541
Rodriguez High School	District	3999	$2,547,363.00	$637.00	76.842711	80.744686	66.366592	80.220055	52.988247
Shelton High School	Charter	1761	$1,056,600.00	$600.00	83.359455	83.725724	93.867121	95.854628	89.892107
Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.350937	83.896082	66.911315	69.663609	65.076453
Wilson High School	Charter	2283	$1,319,574.00	$578.00	83.274201	83.989488	93.867718	96.539641	90.582567
Wright High School	Charter	1800	$1,049,400.00	$583.00	83.682222	83.955000	93.333333	96.611111	90.333333

#### High Performing Schools Impact
In the original dataset, Thomas High School was ranked 2nd best school in terms of Overall Passing Percentage with 90.95%, with the NaN modification it dropped off the top 5 schools entirely allowing Wright High School to capture the 5th spot with a 90.33% Overall Passing Rate.

**Original**
	School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Cabrera High School	Charter	1858	$1,081,356.00	$582.00	83.061895	83.975780	94.133477	97.039828	91.334769
Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.418349	83.848930	93.272171	97.308869	90.948012
Griffin High School	Charter	1468	$917,500.00	$625.00	83.351499	83.816757	93.392371	97.138965	90.599455
Wilson High School	Charter	2283	$1,319,574.00	$578.00	83.274201	83.989488	93.867718	96.539641	90.582567
Pena High School	Charter	962	$585,858.00	$609.00	83.839917	84.044699	94.594595	95.945946	90.540541
**NaN Modified**
School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Cabrera High School	Charter	1858	$1,081,356.00	$582.00	83.061895	83.975780	94.133477	97.039828	91.334769
Griffin High School	Charter	1468	$917,500.00	$625.00	83.351499	83.816757	93.392371	97.138965	90.599455
Wilson High School	Charter	2283	$1,319,574.00	$578.00	83.274201	83.989488	93.867718	96.539641	90.582567
Pena High School	Charter	962	$585,858.00	$609.00	83.839917	84.044699	94.594595	95.945946	90.540541
Wright High School	Charter	1800	$1,049,400.00	$583.00	83.682222	83.955000	93.333333	96.611111	90.333333

#### Low Performing Schools Impact
The bottom 5 schools demonstrate an Overall Passing % range from 52.988 (Rodriguez HS) to 53.539 (Johnson HS). With an overall passing rate so low, even when Thomas HS drops (NaNs) all its reading and math scores, it still manages to avoid the bottom 5 schools as ranked by overall passing percentage. Thus this change did not impact the bottom 5 schools.

**Original**
	School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Rodriguez High School	District	3999	$2,547,363.00	$637.00	76.842711	80.744686	66.366592	80.220055	52.988247
Figueroa High School	District	2949	$1,884,411.00	$639.00	76.711767	81.158020	65.988471	80.739234	53.204476
Huang High School	District	2917	$1,910,635.00	$655.00	76.629414	81.182722	65.683922	81.316421	53.513884
Hernandez High School	District	4635	$3,022,020.00	$652.00	77.289752	80.934412	66.752967	80.862999	53.527508
Johnson High School	District	4761	$3,094,650.00	$650.00	77.072464	80.966394	66.057551	81.222432	53.539172

**NaN Modified**
School Type	Total Students	Total School Budget	Per Student Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Rodriguez High School	District	3999	$2,547,363.00	$637.00	76.842711	80.744686	66.366592	80.220055	52.988247
Figueroa High School	District	2949	$1,884,411.00	$639.00	76.711767	81.158020	65.988471	80.739234	53.204476
Huang High School	District	2917	$1,910,635.00	$655.00	76.629414	81.182722	65.683922	81.316421	53.513884
Hernandez High School	District	4635	$3,022,020.00	$652.00	77.289752	80.934412	66.752967	80.862999	53.527508
Johnson High School	District	4761	$3,094,650.00	$650.00	77.072464	80.966394	66.057551	81.222432	53.539172

#### Thomas High School Impact
As expected, this data change had significant impact to Thomas HS itself. It experienced a 26.36% drop in the % of Passing Math, 27.65% drop in the % Passing Reading, and a 25.87% drop in the overall passing percentage. Clearly there was no impact to the name, type, or budget of the Thomas HS.

**Original**
Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.418349	83.848930	93.272171	97.308869	90.948012
**NaN Modified**
Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.350937	83.896082	66.911315	69.663609	65.076453

#### Math and Reading Scores by Grade
**Original**
**Math**
**Reading**
**NaN Modified**

**Math**

**Reading**

#### Scores by School Spending
**Original**
The following bins were set to segment the scores by school spending/student: (<$584,$585-629,$630-644,$645-675). Thomas HS has a per student spending of $638 and thus we only observe an impact to the $630-644 category.
- 6.47% decrease in % Overall Passing
- 6.91% decrease in % Passing Reading
- 6.59% decrease in % Passing Math
- Negligble changes in Average Math and Reading Scores.

Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Spending Ranges (Per Student)					
<$584	83.5	83.9	93.46	96.61	90.37
$585-629	81.9	83.2	87.13	92.72	81.42
$630-644	78.5	81.6	73.48	84.39	62.86
$645-675	77.0	81.0	66.16	81.13	53.53

**NaN Modified**
Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
Spending Ranges (Per Student)					
<$584	83.5	83.9	93.46	96.61	90.37
$585-629	81.9	83.2	87.13	92.72	81.42
$630-644	78.5	81.6	66.89	77.48	56.39
$645-675	77.0	81.0	66.16	81.13	53.53

#### Scores by School Size
As Thomas HS has 1635 students it is placed in the Medium category (1000-2000) students. Thus there was no observed impact in the Small and Large categories.

In the medium school category, there was negligble change in the Average Math/Reading Scores.
- % Overall Passing dropped 5.17%
- % Passing Reading dropped 5.51%
- % Passing Math dropped 5.27%

**Original**
	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
School Size					
Small (<1000)	83.8	83.9	93.55	96.10	89.88
Medium (1000-2000)	83.4	83.9	93.60	96.79	90.62
Large (2000-5000)	77.7	81.3	69.96	82.77	58.29
**NaN Modified**
Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
School Size					
Small (<1000)	83.8	83.9	93.55	96.10	89.88
Medium (1000-2000)	83.4	83.9	88.33	91.26	85.45
Large (2000-5000)	77.7	81.3	69.96	82.77	58.29

#### Scores by School Type
As Thomas HS is a Charter HS and not a District HS, expectedly we only observe changes to the Charter dataset - the District dataset remained unchanged. 

*Following Trends in the Charter Schools category*
- I had to increase the precision to see a slight drop of .00842 in the Average Math Score, a neglible increase in Average Reading Score of .00589. 
- % Passing Math dropped 3.29%
- % Passing Reading dropped 3.46%
- % Overall Passing dropped 3.23%

**Original**
	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
School Type					
Charter	83.47385	83.89642	93.62	96.59	90.43
District	77.0	81.0	66.55	80.80	53.67
**NaN Modified**
Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
School Type					
Charter	83.46543	83.90231	90.33	93.13	87.20
District	77.0	81.0	66.55	80.80	53.67
