---
description: Cierra un almacén de certificados abierto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Método Store.Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170861"
---
# <a name="storeclose-method"></a>Método Store.Close

\[El **método Close** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Close** cierra un almacén de certificados [*abierto.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxis


```VB
Store.Close()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Después de llamar al método **Close,** [**se**](store.md) destruye el objeto Store.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.1 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**Abrir**](store-open.md)
</dt> </dl>

 

 
