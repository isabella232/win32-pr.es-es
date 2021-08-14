---
description: Determina si el certificado tiene una clave privada asociada. El método lo determina comprobando si la propiedad CERT \_ KEY \_ PROV \_ INFO PROP ID \_ está \_ presente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: ICertificate2::HasPrivateKey (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ac38a62e11d75e21de5fd61dffd821cb4384e4e9b59d2bf11f6e217589ab578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771549"
---
# <a name="icertificate2hasprivatekey-method"></a>ICertificate2::HasPrivateKey (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método HasPrivateKey** determina si el [*certificado*](../secgloss/c-gly.md) tiene una [*clave privada*](../secgloss/p-gly.md) asociada. El método lo determina comprobando si la propiedad CERT \_ KEY \_ PROV \_ INFO PROP ID \_ está \_ presente.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PrivateKey.Open**](privatekey-open.md)
</dt> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
