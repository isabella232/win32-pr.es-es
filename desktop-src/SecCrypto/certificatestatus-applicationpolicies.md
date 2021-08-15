---
description: Devuelve una colección de ID que representa las directivas de aplicación utilizadas para crear el objeto Chain.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Método CertificateStatus.ApplicationPolicies
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
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770447"
---
# <a name="certificatestatusapplicationpolicies-method"></a>Método CertificateStatus.ApplicationPolicies

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la estructura [**X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método ApplicationPolicies** devuelve una [**colección de IDs**](oids.md) que representa las directivas de aplicación usadas para crear el [**objeto Chain.**](chain.md)

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Colección [**de ID.**](oids.md) Cada [**objeto OID**](oid.md) de la colección representa un OID de directiva de aplicación.

## <a name="remarks"></a>Comentarios

Agregue ID de directiva de aplicación a la colección para especificar las directivas de aplicación que se deben usar para crear la cadena de confianza de certificados. Si la colección contiene al menos un [**objeto OID,**](oid.md) se omite el [**objeto EKU**](eku.md) devuelto por el [**método CertificateStatus.EKU.**](certificatestatus-eku.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
