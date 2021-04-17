---
description: Recupera el objeto PolicyInformation que representa la Directiva indizada. Esta es la propiedad predeterminada.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: CertificatePolicies. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690960"
---
# <a name="certificatepoliciesitem-property"></a>CertificatePolicies. Item (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]

La propiedad **Item** recupera el objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva indizada. Esta es la propiedad predeterminada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva indizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
