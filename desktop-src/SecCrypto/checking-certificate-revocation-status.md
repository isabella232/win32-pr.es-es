---
description: CAPICOM no habilita la comprobación de revocación de certificados de forma predeterminada.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Comprobando el estado de revocación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278097"
---
# <a name="checking-certificate-revocation-status"></a>Comprobando el estado de revocación de certificados

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM no habilita la comprobación de revocación de certificados de forma predeterminada. Sin embargo, la comprobación de revocación de certificados se puede habilitar mediante programación para un certificado determinado a través de la propiedad **IsValid. CheckFlag** de un objeto de certificado. Una vez establecido el valor adecuado de **CheckFlag** , el acceso a la propiedad **IsValid. Result** del objeto de certificado o la creación de la ruta de acceso de comprobación del certificado mediante el método de compilación de un objeto Chain fuerza la comprobación de la revocación.

En el ejemplo siguiente, se ha creado una instancia de CERT como un certificado válido de CAPICOM.


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



Lo anterior se aplica a un certificado individual, independientemente de cómo se haya obtenido. La comprobación de la revocación de los certificados en un objeto [**SignedData**](signeddata.md) no es diferente porque el método [**Verify**](signeddata-verify.md) del objeto **SignedData** no se puede usar para este propósito porque si se habilita CAPICOM \_ , la \_ firma y el certificado no \_ \_ provocan la comprobación de CRL.

En su lugar, debe establecerse el valor de **CheckFlag** para el certificado de cada firmante. Considere el ejemplo siguiente donde se ha creado una instancia de sData como un objeto [**SignedData**](signeddata.md) de CAPICOM válido.


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



El ejemplo adicional es el bucle sobre todos los certificados del objeto [**SignedData**](signeddata.md) .

 

 



