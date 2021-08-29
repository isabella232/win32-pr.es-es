---
description: Recupera el objeto PolicyInformation que representa la directiva indizada. Esta es la propiedad predeterminada.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: Propiedad CertificatePolicies.Item
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
ms.openlocfilehash: 001a0cd8e6bab9c6be998f78d467c5b446c639cff994a91865ed99c77ca71caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877925"
---
# <a name="certificatepoliciesitem-property"></a>Propiedad CertificatePolicies.Item

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para recuperar las directivas de certificado.\]

La **propiedad Item** recupera el objeto [**PolicyInformation**](policyinformation.md) que representa la directiva indizada. Esta es la propiedad predeterminada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**PolicyInformation**](policyinformation.md) que representa la directiva indizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
