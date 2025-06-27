# ATM-Project
Lessons and test


用例图 user case diagram

<img width="805" alt="image" src="https://github.com/user-attachments/assets/27976afe-8c15-4658-931a-6eb9e6a3d6fc" />

用例描述
1. withdrawCash
<img width="674" alt="image" src="https://github.com/user-attachments/assets/da4332dc-7eae-478a-a8ba-2f1f5100ba23" />

 2. <b>checkBalance</b>
   <img width="693" alt="image" src="https://github.com/user-attachments/assets/c0ae9254-5433-4432-aaf3-03374e43ce39" />
3. depositFunds
<img width="685" alt="image" src="https://github.com/user-attachments/assets/d4579b6c-e0cd-46f3-961b-b868aa19a0e4" />

4. manageBankCard
<html>
 <table>
	<tr>
		<td><b>UseCase Name:</b></td>
		<td><span name ="UCmanageBankCard">manageBankCard</span></td>
	</tr>
	<tr>
		<td><b>UseCase ID:</b></td>
		<td>UC4</td>
	</tr>
	<tr>
		<td><b>Brief Description:</b></td>
		<td>The bank clerk manages bank card information, including entering, inquiring, modifying and deleting of bank card information</td>
	</tr>
	<tr>
		<td><b>Involved Actor:</b></td>
	<td><a href="#ACTORBankClerk">BankClerk</a></td>
	</tr>
	<tr>
		<td><b>Preconditions:</b></td>
		<td><ol></ol></td>
	</tr>
	<tr>
		<td><b>Postconditions:</b></td>
		<td><ol></ol></td>
	</tr>						
	<tr>
		<td><b>Basic Path:</b></td>
	<td></td>
	</tr>
	<tr>
		<td><b>Alternative Path:</b></td>
		<td></td>
	</tr>
	</table>
</html>
5. manageUser
<html>
 <table>
	<tr>
		<td><b>UseCase Name:</b></td>
		<td><span name ="UCmanageUser">manageUser</span></td>
	</tr>
	<tr>
		<td><b>UseCase ID:</b></td>
		<td>UC5</td>
	</tr>
	<tr>
		<td><b>Brief Description:</b></td>
		<td>The bank clerk manages bank card information, including entering, inquiring, modifying and deleting of bank card information</td>
	</tr>
	<tr>
		<td><b>Involved Actor:</b></td>
	<td><a href="#ACTORBankClerk">BankClerk</a></td>
	</tr>
	<tr>
		<td><b>Preconditions:</b></td>
		<td><ol></ol></td>
	</tr>
	<tr>
		<td><b>Postconditions:</b></td>
		<td><ol></ol></td>
	</tr>						
	<tr>
		<td><b>Basic Path:</b></td>
	<td></td>
	</tr>
	<tr>
		<td><b>Alternative Path:</b></td>
		<td></td>
	</tr>
	</table>
</html>
6. cardIdentification
<html>
 <table>
	<tr>
		<td><b>UseCase Name:</b></td>
		<td><span name ="UCcardIdentification">cardIdentification</span></td>
	</tr>
	<tr>
		<td><b>UseCase ID:</b></td>
		<td>UC6</td>
	</tr>
	<tr>
		<td><b>Brief Description:</b></td>
		<td>The system verifies the card</td>
	</tr>
	<tr>
		<td><b>Involved Actor:</b></td>
	<td></td>
	</tr>
	<tr>
		<td><b>Preconditions:</b></td>
		<td><ol></ol></td>
	</tr>
	<tr>
		<td><b>Postconditions:</b></td>
		<td><ol></ol></td>
	</tr>						
	<tr>
		<td><b>Basic Path:</b></td>
	<td></td>
	</tr>
	<tr>
		<td><b>Alternative Path:</b></td>
		<td></td>
	</tr>
	</table>
</html>


实体分析

<img width="679" alt="image" src="https://github.com/user-attachments/assets/c2a39bf8-c1de-40f1-9200-25a3d081adc0" />

<b>E1 - BankCard</b>

<table>
	<tr>
		<td><b>Entity Name:</b></td>
		   <td colspan="3"><span name ="CLASSBankCard">BankCard</span></td>
	</tr>
	<tr>
		<td><b>Entity ID:</b></td>
		   <td colspan="3">E1</td>
	</tr>
	<tr>
	    <td><b>Entity Description:</b></td>
	    <td colspan="3">The BankCrad is a card that can deposit or withdraw money</td>
	</tr>
	<tr>
	    <td><b>Attribute Name</b></td>
		<td><b>Attribute Type</b></td>
		<td colspan="2"><b>Attribute Description</b></td>
	</tr>
	<tr>
	    <td>CardID</td>
	<td>Integer</td>
	<td colspan="2">The CardID of BankCard</td>
					</tr>
	<tr>
	    <td>CardStatus</td>
	<td>[NORMAL|SUSPEND|CANNEL]</td>
	<td colspan="2">The CardStatus of BankCard</td>
					</tr>
	<tr>
	    <td>Catalog</td>
	<td>[CREDIT|DESPOSIT]</td>
	<td colspan="2">The Catalog of BankCard</td>
					</tr>
	<tr>
	    <td>Password</td>
	<td>Integer</td>
	<td colspan="2">The Password of BankCard</td>
					</tr>
	<tr>
	    <td>Balance</td>
	<td>Real</td>
	<td colspan="2">The Balance of BankCard</td>
					</tr>
	<tr>
	    <td><b>Relationship Name</b></td>
	<td><b>Related Entity</b></td>
	<td><b>Relationship Type</b></td>
	<td><b>Relationship Description</b></td>
	</tr>
		<tr>
			<td>BelongedUser</td>
			<td><a href="#CLASSUser">User</a></td>
			<td>Association</td>
		<td>Many BankCard are linked with one User</td>
	</tr>
	</table>


<b>E2 - User</b>

<table>
	<tr>
		<td><b>Entity Name:</b></td>
		   <td colspan="3"><span name ="CLASSUser">User</span></td>
	</tr>
	<tr>
		<td><b>Entity ID:</b></td>
		   <td colspan="3">E2</td>
	</tr>
	<tr>
	    <td><b>Entity Description:</b></td>
	    <td colspan="3">The user is the holder of the bank card</td>
	</tr>
	<tr>
	    <td><b>Attribute Name</b></td>
		<td><b>Attribute Type</b></td>
		<td colspan="2"><b>Attribute Description</b></td>
	</tr>
	<tr>
	    <td>UserID</td>
	<td>Integer</td>
	<td colspan="2">The UserID of User</td>
					</tr>
	<tr>
	    <td>Name</td>
	<td>String</td>
	<td colspan="2">The Name of User</td>
					</tr>
	<tr>
	    <td>Address</td>
	<td>String</td>
	<td colspan="2">The Address of User</td>
					</tr>
	<tr>
	    <td><b>Relationship Name</b></td>
	<td><b>Related Entity</b></td>
	<td><b>Relationship Type</b></td>
	<td><b>Relationship Description</b></td>
	</tr>
		<tr>
			<td>OwnedCard</td>
			<td><a href="#CLASSBankCard">BankCard</a></td>
			<td>Association</td>
		<td>One User is linked with many BankCard</td>
	</tr>
	</table>



​	 
