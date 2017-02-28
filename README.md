var xmlFilePath = tags['Absolute Path'];
xmlFilePath = xmlFilePath.get(0).replace("\\","/");
var xmlText = textFileContent(xmlFilePath);
//========================================
//========================================
//	Parent Container	:	CollateralCollectionCategorization
//========================================
//========================================
//	Target	:	CollateralCollectionAmortizationCategoryTypeCode
//========================================

//if (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") 
 //(tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")
	//(tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] =="Fixed");{
		//tags['CollateralCollectionAmortizationCategoryTypeCode'] = '1'
//}
//else   if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] == "AdjustableRate"){
		//tags['CollateralCollectionAmortizationCategoryTypeCode'] = '2'
	//}
//========================================
//	Target	:	CollateralCollectionBalloonPaymentIndicator
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if(tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralPoolType'] !== ""){


	tags['temp'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolBalloonIndicator']
if(temp == "true"){
	var CollateralCollectionBalloonPaymentIndicator = 'Y'
}
else if(temp == "false"){
	var CollateralCollectionBalloonPaymentIndicator = 'N'
}
//tags['CollateralCollectionBalloonPaymentIndicator'] = CollateralCollectionBalloonPaymentIndicator
}
//========================================
//	Target	:	CollateralAccrualRateMethodTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if(tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAccrualRateStructureType'] !== ""){
	if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] == "AdjustableRate"){
tags['CollateralAccrualRateMethodTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAccrualRateStructureType']
		}
	}
}
//========================================
//	Target	:	CollateralAmortizationTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['CollateralAmortizationTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType']
}
//========================================
//	Target	:	CollateralCollectionDeliveryTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['CollateralCollectionDeliveryTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralPoolDeliveryType']

var CollateralCollectionDeliveryTypeCode = '1'
tags['CollateralCollectionDeliveryTypeCode'] = CollateralCollectionDeliveryTypeCode
}

//========================================
//	Target	:	CollateralCollectionActionTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if(tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralCollectionLastActionType'] !== ""){
tags['CollateralCollectionActionTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralCollectionLastActionType']
} 
	else{

tags['CollateralCollectionActionTypeCode'] = "1"
	}
}
//========================================
//	Target	:	CollateralLoanTypeCodeCollateralLoanTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['CollateralLoanTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolMortgageType']}
else{
	tags['CollateralLoanTypeCode'] = "1"
}
//========================================
//	Target	:	IssuerPoolIdentifier
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['IssuerPoolIdentifier'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolIdentifier']
}
//========================================
//	Target	:	IssuerPoolPrefixCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['IssuerPoolPrefixCode'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolPrefixIdentifier']
}
//========================================
//	Target	:	IssuerPoolSubtypeDescription
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] == "AdjustableRate"){
tags['IssuerPoolSubtypeDescription'] = tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/InvestorPoolSubtypeDescription']
	}
}

//========================================
//	Target	:	SecurityRequestedIssueDate
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	tags['SecurityRequestedIssueDate'] = xpath(xmlText,"//*:DEAL_SETS/*:DEAL_SET/*:POOL/*:EXTENSION/*:NEW_ISSUE_DETAIL/*:SecurityIssueDate/text()");
}
//========================================
//	Target	:	SecurityTypeCode
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if(tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralPoolType'] !== ""){
tags['SecurityTypeCode'] = tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralPoolType']
	}
}
//========================================
//	Target	:	CollateralMaximumAccrualRatePercent
//========================================
if (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns"){
	if (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns"){
		if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAccrualRateStructureType'] == "StatedStructure"){
			if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] == "AdjustableRate"){
		tags['CollateralMaximumAccrualRatePercent'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAccrualRateStructureType']
			}	
		}
	}
}
//=======================================
//	Target	:	CollateralMinimumAccrualRatePercent
//========================================
if (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns"){
	if (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns"){
		if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAccrualRateStructureType'] == "StatedStructure"){
			if (tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolAmortizationType'] == "AdjustableRate"){
		tags['CollateralMinimumAccrualRatePercent'] = tags['DEAL_SETS/DEAL_SET/POOL/POOL_DETAIL/PoolMinimumAccrualRatePercent']
			}
		}
	}
}	

//=======================================
//	Target	:	CollateralTransferTypeEnumeration
//========================================
if ((tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralAndWireIns") || (tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/SecuritizationRequestType'] == "ShelfWithCollateralNoWireIns")){
	if(tags['DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/PoolTransferType'] !== ""){
	tags['CollateralTransferTypeEnumeration'] = xpath(xmlText,"//*:DEAL_SETS/*:DEAL_SET/*:POOL/*:EXTENSION/*:NEW_ISSUE_DETAIL/*:PoolTransferType/text()");
}
}
}
tags['CollateralCollectionDeliveryTypeCode'] = dbQuery("IDS", "SELECT COLT_CLCTN_DLRY_TYP_CD FROM COLT_CLCTN_DLRY_TYP_REF WHERE COLT_CLCTN_DLRY_TYP_NME = '%%DEAL_SETS/DEAL_SET/POOL/EXTENSION/NEW_ISSUE_DETAIL/CollateralPoolDeliveryType%%'")
