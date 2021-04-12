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
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="7dac6-103">Comprobando el estado de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="7dac6-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="7dac6-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7dac6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7dac6-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7dac6-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="7dac6-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="7dac6-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="7dac6-107">CAPICOM no habilita la comprobación de revocación de certificados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7dac6-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="7dac6-108">Sin embargo, la comprobación de revocación de certificados se puede habilitar mediante programación para un certificado determinado a través de la propiedad **IsValid. CheckFlag** de un objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="7dac6-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="7dac6-109">Una vez establecido el valor adecuado de **CheckFlag** , el acceso a la propiedad **IsValid. Result** del objeto de certificado o la creación de la ruta de acceso de comprobación del certificado mediante el método de compilación de un objeto Chain fuerza la comprobación de la revocación.</span><span class="sxs-lookup"><span data-stu-id="7dac6-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="7dac6-110">En el ejemplo siguiente, se ha creado una instancia de CERT como un certificado válido de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="7dac6-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


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



<span data-ttu-id="7dac6-111">Lo anterior se aplica a un certificado individual, independientemente de cómo se haya obtenido.</span><span class="sxs-lookup"><span data-stu-id="7dac6-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="7dac6-112">La comprobación de la revocación de los certificados en un objeto [**SignedData**](signeddata.md) no es diferente porque el método [**Verify**](signeddata-verify.md) del objeto **SignedData** no se puede usar para este propósito porque si se habilita CAPICOM \_ , la \_ firma y el certificado no \_ \_ provocan la comprobación de CRL.</span><span class="sxs-lookup"><span data-stu-id="7dac6-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="7dac6-113">En su lugar, debe establecerse el valor de **CheckFlag** para el certificado de cada firmante.</span><span class="sxs-lookup"><span data-stu-id="7dac6-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="7dac6-114">Considere el ejemplo siguiente donde se ha creado una instancia de sData como un objeto [**SignedData**](signeddata.md) de CAPICOM válido.</span><span class="sxs-lookup"><span data-stu-id="7dac6-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


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



<span data-ttu-id="7dac6-115">El ejemplo adicional es el bucle sobre todos los certificados del objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="7dac6-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



