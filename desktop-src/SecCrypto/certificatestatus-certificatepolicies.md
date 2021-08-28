---
description: Devuelve una colección de ID que representa las directivas de certificado usadas para crear el objeto Chain.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Método CertificateStatus.CertificatePolicies
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
ms.openlocfilehash: e4d6507446bf15d00d8e388699ee0c0892c8755b94913d18657634311db57ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126715"
---
# <a name="certificatestatuscertificatepolicies-method"></a>Método CertificateStatus.CertificatePolicies

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la estructura [**X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método CertificatePolicies** devuelve una [**colección de IDs**](oids.md) que representa las directivas de certificado usadas para crear el [**objeto Chain.**](chain.md)

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Colección [**de ID.**](oids.md) Cada [**objeto OID**](oid.md) de la colección representa un OID de directiva de certificado.

## <a name="remarks"></a>Comentarios

Agregue ID de directiva de certificado a la colección para especificar las directivas de certificado que se deben usar para crear la cadena de confianza de certificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
