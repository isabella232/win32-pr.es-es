---
description: Establece o recupera el período de tiempo antes de que se determine que una dirección URL es inaccesible.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Propiedad CertificateStatus.UrlRetrievalTimeout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770095"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>Propiedad CertificateStatus.UrlRetrievalTimeout

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la estructura [**X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad UrlRetrievalTimeout** establece o recupera el período de tiempo antes de que se determine que una dirección URL es inaccesible.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de segundos antes de que se determine que no se puede acceder a una dirección URL.

## <a name="remarks"></a>Comentarios

Si no se establece esta propiedad, el tiempo de espera predeterminado es de 15 segundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
