---
description: Proporciona métodos de enumeración estándar de COM para la interfaz IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaz IEnumPStoreProviders (pstore. h)
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
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661179"
---
# <a name="ienumpstoreproviders-interface"></a>Interfaz IEnumPStoreProviders

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Proporciona métodos de enumeración estándar de COM para la interfaz [**IPStore**](ipstore.md) .

## <a name="members"></a>Miembros

La interfaz **IEnumPStoreProviders** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumPStoreProviders** tiene estos métodos.



| Método                                      | Descripción                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumpstoreproviders-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoreproviders-next.md)   | Obtiene el siguiente proveedor especificado en la secuencia de enumeración.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Se restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoreproviders-skip.md)   | Omite el proveedor especificado en la secuencia de enumeración.<br/>                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
