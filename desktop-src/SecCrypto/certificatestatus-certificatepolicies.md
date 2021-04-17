---
description: Devuelve una colección de OID que representa las directivas de certificado utilizadas para crear el objeto de cadena.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670779"
---
# <a name="certificatestatuscertificatepolicies-method"></a>CertificateStatus. CertificatePolicies, método

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **CertificatePolicies** devuelve una colección de [**OID**](oids.md) que representa las directivas de certificado utilizadas para crear el objeto de [**cadena**](chain.md) .

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Colección de [**OID**](oids.md) . Cada objeto [**OID**](oid.md) de la colección representa un OID de la Directiva de certificado.

## <a name="remarks"></a>Observaciones

Agregue OID de directiva de certificados a la colección para especificar las directivas de certificado que se deben usar para generar la cadena de confianza de certificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
