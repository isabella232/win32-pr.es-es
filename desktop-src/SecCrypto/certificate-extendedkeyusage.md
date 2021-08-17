---
description: Devuelve un objeto ExtendedKeyUsage que indica los usos válidos del certificado.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: ICertificate2::ExtendedKeyUsage (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c496faf8c28c6dc9abacf75156f53a91cf7fc4d71b4ef469b64d2daa424d1a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771659"
---
# <a name="icertificate2extendedkeyusage-method"></a>ICertificate2::ExtendedKeyUsage (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método ExtendedKeyUsage** devuelve [**un objeto ExtendedKeyUsage**](extendedkeyusage.md) que indica los usos válidos del certificado.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El [**objeto ExtendedKeyUsage**](extendedkeyusage.md) asociado al certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
