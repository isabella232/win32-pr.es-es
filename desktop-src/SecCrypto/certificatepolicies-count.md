---
description: Recupera el número de objetos PolicyInformation de la colección.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies. Count (propiedad)
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
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691004"
---
# <a name="certificatepoliciescount-property"></a>CertificatePolicies. Count (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]

La propiedad **Count** recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**PolicyInformation**](policyinformation.md) de la colección. Cada objeto **PolicyInformation** representa una única directiva de certificado en la colección.

## <a name="remarks"></a>Observaciones

La propiedad **Count** se puede usar para especificar el último objeto [**PolicyInformation**](policyinformation.md) de la colección al recuperar un objeto **PolicyInformation** específico mediante la propiedad [**CertificatePolicies. Item**](certificatepolicies-item.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
