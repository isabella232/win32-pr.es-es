---
description: Proporciona los métodos de enumeración estándar de COM para la interfaz IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaz IEnumPStoreItems (pstore. h)
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
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660371"
---
# <a name="ienumpstoreitems-interface"></a>Interfaz IEnumPStoreItems

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Proporciona los métodos de enumeración estándar de COM para la interfaz [**IPStore**](ipstore.md) .

## <a name="members"></a>Miembros

La interfaz **IEnumPStoreItems** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreItems** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumPStoreItems** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumpstoreitems-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoreitems-next.md)   | Obtiene el siguiente elemento de datos especificado en la secuencia de enumeración.<br/>                          |
| [**Reset**](ienumpstoreitems-reset.md) | Se restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoreitems-skip.md)   | Omite el elemento de datos especificado en la secuencia de enumeración.<br/>                              |



 

## <a name="remarks"></a>Observaciones

Es necesario liberar cada elemento después de enumerarlo. También se debe liberar el objeto de enumerador cuando ya no se utiliza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
