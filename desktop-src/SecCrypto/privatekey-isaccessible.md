---
description: Devuelve un valor booleano que indica si se puede tener acceso a la clave privada.
ms.assetid: ee5e89af-745e-4a4d-9943-fecbaee5d3e3
title: PrivateKey. IsAccessible, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsAccessible
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9997fad702ab1eddbf4c60fa2304df8185ef4c63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690661"
---
# <a name="privatekeyisaccessible-method"></a>PrivateKey. IsAccessible, método

\[El método **IsAccessible** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **IsAccessible** devuelve un valor booleano que indica si se puede tener acceso a la clave privada.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.IsAccessible()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si es true, se puede tener acceso a la clave privada.

## <a name="remarks"></a>Observaciones

El valor devuelto de este método depende del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado. Este método devolverá un valor de confianza si se usa un CSP de Microsoft. Si el CSP no es un CSP de Microsoft, el valor devuelto no puede ser de confianza para ser preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
