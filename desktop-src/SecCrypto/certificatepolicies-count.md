---
description: Recupera el número de objetos PolicyInformation de la colección.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Propiedad CertificatePolicies.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 405fbc928f6ff553abe3cd55d3f6e08a1aed13ef46093f912b6b08af45ec2c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771054"
---
# <a name="certificatepoliciescount-property"></a>Propiedad CertificatePolicies.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para recuperar las directivas de certificado.\]

La **propiedad Count** recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**PolicyInformation**](policyinformation.md) de la colección. Cada **objeto PolicyInformation** representa una única directiva de certificado en la colección.

## <a name="remarks"></a>Comentarios

La **propiedad Count** se puede usar para especificar el último objeto [**PolicyInformation**](policyinformation.md) de la colección al recuperar un objeto **PolicyInformation** específico mediante la [**propiedad CertificatePolicies.Item.**](certificatepolicies-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
