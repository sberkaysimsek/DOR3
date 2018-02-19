<!DOCTYPE html>
<html>
<head>
	<title></title>
	<meta charset="UTF-8"/>

</head>
<body>

	<?php 
	include 'func.php';	
	function hataAra($metin)
	{	
		for ($t=0; $t<count($Email__NotExist) ; $t++) 
		{ 	
			$aranan = strpos($metin,$Email__NotExist[$t]);
			if ($aranan!==false) 
			{
				return "Hard";
			}
		}
	}

	$mailbox = imap_open ("{xxx.com:143/imap/notls}INBOX", "zzz", "yyy");

	$check=imap_check($mailbox);

	print("<PRE>"); 
	print("Date most recent message : " . $check->Date); 
	print("<BR>"); 
	print("Connection type : " . $check->Driver); 
	print("<BR>"); 
	print("Name of the mailbox : " . $check->Mailbox); 
	print("<BR>"); 
	print("Number of messages : " . $check->Nmsgs); 
	print("<BR>"); 
	print("Number of recent messages : " . $check->Recent); 
	print("<BR>"); 
	print("</PRE>-----------------------------");

	echo '<table border="1" align="center">
			<tr>
				<td>Sender</td>
				<td>Date</td>
				<td>Error</td>
			</tr>	
	';

	for ($i=1; $i < $check->Nmsgs; $i++)
	{
		$header = imap_header($mailbox, $i);
		$bodyText = imap_body($mailbox,$i);
		
		for ($t=0; $t <count($Email__NotExist) ; $t++) 
		{ 	
			$aranan = strpos($bodyText,$Email__NotExist[$t]);
			if ($aranan!==false) 
			{
				echo'<tr>
						<td>'.$header->fromaddress.'</td>
						<td>'.$header->Date.'</td>
						<td>'.$Email__NotExist[$t].'</td>
					</tr>';
			}
		}
	}
	echo('</table>');
	imap_close($mailbox);
	?>
	
</body>
</html>
