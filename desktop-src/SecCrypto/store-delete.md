---
description: Elimina el almacén de certificados representado por el objeto de almacén actual.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650209"
---
# <a name="storedelete-method"></a>Store. Delete (método)

\[El método **Delete** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Delete** elimina el [*almacén de certificados*](../secgloss/c-gly.md) representado por el objeto de [**almacén**](certificate.md) actual. Este método elimina solo almacenes que no son del sistema.

## <a name="syntax"></a>Sintaxis


```VB
Store.Delete()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los siguientes almacenes son almacenes del sistema y no se pueden eliminar:

-   My
-   Root
-   Confianza
-   CA
-   UserDS
-   TrustedPublisher
-   No permitida.
-   AuthRoot
-   TrustedPeople

El método **Delete** devuelve un error si se llama desde un script Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
