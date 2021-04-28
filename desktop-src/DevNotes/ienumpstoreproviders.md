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
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089353"
---
# <a name="ienumpstoreproviders-interface"></a>IEnumPStoreProviders (interfaz)

\[El almacenamiento protegido (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Proporciona métodos de enumeración com estándar para la [**interfaz IPStore.**](ipstore.md)

## <a name="members"></a>Miembros

La **interfaz IEnumPStoreProviders** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreProviders también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumPStoreProviders** tiene estos métodos.



| Método                                      | Descripción                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumpstoreproviders-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoreproviders-next.md)   | Obtiene el siguiente proveedor especificado en la secuencia de enumeración.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoreproviders-skip.md)   | Omite el proveedor especificado en la secuencia de enumeración.<br/>                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
