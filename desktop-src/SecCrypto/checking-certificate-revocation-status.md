---
description: CAPICOM no habilita la comprobación de revocación de certificados de forma predeterminada.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Comprobación del estado de revocación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769545"
---
# <a name="checking-certificate-revocation-status"></a>Comprobación del estado de revocación de certificados

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM no habilita la comprobación de revocación de certificados de forma predeterminada. Sin embargo, la comprobación de revocación de certificados se puede habilitar mediante programación para un certificado determinado a través de la **propiedad IsValid.CheckFlag** de un objeto Certificate. Una vez establecido el valor adecuado de **CheckFlag,** el acceso a la propiedad **IsValid.Result** del objeto Certificate o la compilación de la ruta de verificación del certificado mediante el método Build de un objeto Chain fuerza la comprobación de revocación.

En el ejemplo siguiente, se ha crea una instancia de cert como un certificado CAPICOM válido.


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



Lo anterior se aplica a un certificado individual, independientemente de cómo se haya obtenido. La realización de la comprobación de revocación en los certificados de un objeto [**SignedData**](signeddata.md) no es diferente porque el método [**Verify**](signeddata-verify.md) del objeto **SignedData** no se puede usar para este propósito porque la habilitación de CAPICOM VERIFY SIGNATURE AND CERTIFICATE no provoca la comprobación de \_ \_ \_ \_ CRL.

En su lugar, se debe establecer **CheckFlag** para el certificado de cada firmante. Considere el ejemplo siguiente en el que se ha iniciado una instancia de sData como un objeto [**SignedData**](signeddata.md) capicom válido.


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



El ejemplo adicional es el bucle sobre todos los certificados del [**objeto SignedData.**](signeddata.md)

 

 



