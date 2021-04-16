---
description: Proporciona métodos de enumeración estándar de COM para la interfaz IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaz IEnumPStoreTypes (pstore. h)
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
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650114"
---
# <a name="ienumpstoretypes-interface"></a>Interfaz IEnumPStoreTypes

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Proporciona métodos de enumeración estándar de COM para la interfaz [**IPStore**](ipstore.md) .

## <a name="members"></a>Miembros

La interfaz **IEnumPStoreTypes** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreTypes** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumPStoreTypes** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumpstoretypes-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumpstoretypes-next.md)   | Obtiene el siguiente tipo de proveedor especificado en la secuencia de enumeración.<br/>                      |
| [**Reset**](ienumpstoretypes-reset.md) | Se restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumpstoretypes-skip.md)   | Omite el tipo de proveedor especificado en la secuencia de enumeración.<br/>                          |



 

## <a name="remarks"></a>Observaciones

El objeto de enumerador debe liberarse cuando ya no se use.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
