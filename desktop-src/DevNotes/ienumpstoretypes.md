---
description: 'Interfaz IEnumPStoreTypes: proporciona métodos de enumeración com estándar para la interfaz IPStore.'
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaz IEnumPStoreTypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 668ed2b7177344004cb4b872ff47a5924fdcc1778cfbfbb3c6d3d447b624546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955964"
---
# <a name="ienumpstoretypes-interface"></a>Interfaz IEnumPStoreTypes

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Proporciona métodos de enumeración estándar com para la [**interfaz IPStore.**](ipstore.md)

## <a name="members"></a>Miembros

La **interfaz IEnumPStoreTypes** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreTypes** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumPStoreTypes** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienumpstoretypes-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoretypes-next.md)   | Obtiene el siguiente tipo de proveedor especificado en la secuencia de enumeración.<br/>                      |
| [**Restablecer**](ienumpstoretypes-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoretypes-skip.md)   | Omite el tipo de proveedor especificado en la secuencia de enumeración.<br/>                          |



 

## <a name="remarks"></a>Comentarios

El objeto enumerador debe liberarse cuando ya no se esté utilizando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
