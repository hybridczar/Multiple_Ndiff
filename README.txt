This modifided version of ndiff allows the user to input multiple nmap scans at once and compare them against a baseline.

USAGE:
	mndiff (ndiff switches optional)(baseline scan) (scan 1) (scan 2) ... (scan n)

New Functions:

Host_Sum(a,b)

This function takes two lists of sorted hosts from a provided nmap scan and checks to see which ones have remained constant during the scan.

Exec_compare(a,b)

This function takes in two lists of sorted IP addresses and checks to see which ones are consistent and inconsistent. The ouput is then used to formulate an executive summary.

Modifications to the Main() function where made as well.
Main() now allows multiple scans to be looped through, during this loop it displays localized consitent and inconsistent hosts as well as an executive summary displayed at the end of all the scan comparisons.

How to adjust the search critera:

This can be done by modifying Host_sum(a,b) to search for different items within the hosts in each local comparison. Currently it checks host.get_id() and only handles the results from that function.