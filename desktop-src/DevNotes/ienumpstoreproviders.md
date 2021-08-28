---
description: 'Interfaz IEnumPStoreProviders: proporciona métodos de enumeración com estándar para la interfaz IPStore.'
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaz IEnumPStoreProviders (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: eb73345dd594f3583b4a6cfbc6e0462848d85de0e9470e6bc8177574a2fff20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017713"
---
# <a name="ienumpstoreproviders-interface"></a>Interfaz IEnumPStoreProviders

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Proporciona métodos de enumeración com estándar para la [**interfaz IPStore.**](ipstore.md)

## <a name="members"></a>Miembros

La **interfaz IEnumPStoreProviders** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreProviders también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumPStoreProviders** tiene estos métodos.



| Método                                      | Descripción                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienumpstoreproviders-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoreproviders-next.md)   | Obtiene el siguiente proveedor especificado en la secuencia de enumeración.<br/>                           |
| [**Restablecer**](ienumpstoreproviders-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoreproviders-skip.md)   | Omite el proveedor especificado en la secuencia de enumeración.<br/>                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
