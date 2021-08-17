---
description: Devuelve un objeto KeyUsage que indica el uso de clave válido del certificado.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: ICertificate2::KeyUsage (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7ce3fc7246a7962ea852167cdc93e25e4d8ab11976eb3cf2868642bb906c41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771551"
---
# <a name="icertificate2keyusage-method"></a>ICertificate2::KeyUsage (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método KeyUsage** devuelve un [**objeto KeyUsage**](keyusage.md) que indica el uso de clave válido del certificado.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
