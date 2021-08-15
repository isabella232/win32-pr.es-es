---
description: Proporciona los métodos de enumeración estándar COM para la interfaz IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaz IEnumPStoreItems (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f5952dbaff2560ae4c2fc59af73246c2cd5c1d050bb53bc3c7b9091c8a39822f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542245"
---
# <a name="ienumpstoreitems-interface"></a>IEnumPStoreItems (interfaz)

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Proporciona los métodos de enumeración estándar COM para la [**interfaz IPStore.**](ipstore.md)

## <a name="members"></a>Miembros

La **interfaz IEnumPStoreItems** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreItems** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumPStoreItems** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienumpstoreitems-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoreitems-next.md)   | Obtiene el siguiente elemento de datos especificado en la secuencia de enumeración.<br/>                          |
| [**Restablecer**](ienumpstoreitems-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoreitems-skip.md)   | Omite el elemento de datos especificado en la secuencia de enumeración.<br/>                              |



 

## <a name="remarks"></a>Comentarios

Es necesario liberar cada elemento después de enumerarlo. El objeto enumerador también debe liberarse cuando ya no se esté utilizando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
