---
description: La interfaz IEnumTime proporciona métodos de enumeración com estándar para la interfaz ITTime. El método ITTimeCollection::get \_ EnumerationIf devuelve un puntero a IEnumTime.
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaz IEnumTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c79d780374bcf121dcb5010aef51725f9836e511bed4b86c855970bb47b838e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992205"
---
# <a name="ienumtime-interface"></a>Interfaz IEnumTime

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IEnumTime proporciona métodos** de enumeración com estándar para la [**interfaz ITTime.**](ittime.md) El [**método ITTimeCollection::get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) devuelve un puntero a **IEnumTime**.

## <a name="members"></a>Miembros

La **interfaz IEnumTime** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumTime también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumTime** tiene estos métodos.



| Método                           | Descripción                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienumtime-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumtime-next.md)   | Obtiene el siguiente número especificado de elementos de la secuencia de enumeración.<br/>                 |
| [**Restablecer**](ienumtime-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumtime-skip.md)   | Omite el siguiente número especificado de elementos en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

