---
description: Elimina el almacén de certificados representado por el objeto Store actual.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Método Store.Delete
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
ms.openlocfilehash: 36c4a02795468ca719790707356b12a1aa24c1882a0cf57faa9e0454af33467a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972656"
---
# <a name="storedelete-method"></a>Método Store.Delete

\[El **método** Delete está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Delete** elimina el almacén de [*certificados*](../secgloss/c-gly.md) representado por el objeto [**Store**](certificate.md) actual. Este método elimina solo los almacenes que no son del sistema.

## <a name="syntax"></a>Sintaxis


```VB
Store.Delete()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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

El **método Delete** devuelve un error si se llama desde un script web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
