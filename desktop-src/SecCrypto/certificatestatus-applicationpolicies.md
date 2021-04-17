---
description: Devuelve una colección de OID que representa las directivas de aplicación utilizadas para crear el objeto de cadena.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. ApplicationPolicies, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690170"
---
# <a name="certificatestatusapplicationpolicies-method"></a>CertificateStatus. ApplicationPolicies, método

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **ApplicationPolicies** devuelve una colección de [**OID**](oids.md) que representa las directivas de aplicación utilizadas para crear el objeto de [**cadena**](chain.md) .

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Colección de [**OID**](oids.md) . Cada objeto [**OID**](oid.md) de la colección representa un OID de directiva de aplicación.

## <a name="remarks"></a>Observaciones

Agregue OID de directiva de aplicación a la colección para especificar las directivas de aplicación que se deben usar para generar la cadena de confianza de certificados. Si la colección contiene al menos un objeto [**OID**](oid.md) , se omite el objeto [**EKU**](eku.md) devuelto por el método [**CertificateStatus. EKU**](certificatestatus-eku.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
