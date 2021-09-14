---
description: La interfaz IEnumMedia proporciona métodos de enumeración com estándar para la interfaz ITMedia. El método ITMediaCollection::get \_ EnumerationIf devuelve un puntero a IEnumMedia.
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interfaz IEnumMedia (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068759"
---
# <a name="ienummedia-interface"></a>Interfaz IEnumMedia

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IEnumMedia proporciona métodos** de enumeración com estándar para la [**interfaz ITMedia.**](itmedia.md) El [**método ITMediaCollection::get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) devuelve un puntero a **IEnumMedia**.

## <a name="members"></a>Members

La **interfaz IEnumMedia** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumMedia también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumMedia** tiene estos métodos.



| Método                            | Descripción                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienummedia-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienummedia-next.md)   | Obtiene el siguiente número especificado de elementos de la secuencia de enumeración.<br/>                 |
| [**Reset**](ienummedia-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Saltar**](ienummedia-skip.md)   | Omite el siguiente número especificado de elementos en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

