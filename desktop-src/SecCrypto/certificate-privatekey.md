---
description: Establece o recupera la clave privada asociada al certificado.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propiedad Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671847"
---
# <a name="certificateprivatekey-property"></a>Propiedad Certificate. PrivateKey

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **PrivateKey** establece o recupera la clave privada asociada al certificado. Esta propiedad se incorporó en CAPICOM 2,0.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**PrivateKey**](privatekey.md) que representa la clave privada asociada al certificado.

## <a name="remarks"></a>Observaciones

Al establecer la propiedad **PrivateKey** en Nothing, se quita la asociación entre la clave privada y el certificado, pero no se elimina la clave privada. Para eliminar la clave privada, llame al método [**privatekey. Delete**](privatekey-delete.md) y, a continuación, establezca esta propiedad en Nothing.

Esta propiedad produce CAPICOM \_ E \_ no \_ se permite cuando se establece desde una aplicación basada en Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
