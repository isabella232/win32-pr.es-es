---
description: La interfaz IEnumMedia proporciona métodos de enumeración com estándar para la interfaz ITMedia. El método ITMediaCollection::get \_ EnumerationIf devuelve un puntero a IEnumMedia.
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interfaz IEnumMedia (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e180e861e452d841153127f6476ed5d8f5924480877eac78c4634e86437189f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660755"
---
# <a name="ienummedia-interface"></a>Interfaz IEnumMedia

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IEnumMedia proporciona métodos** de enumeración com estándar para la [**interfaz ITMedia.**](itmedia.md) El [**método ITMediaCollection::get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) devuelve un puntero a **IEnumMedia**.

## <a name="members"></a>Miembros

La **interfaz IEnumMedia** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumMedia también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumMedia** tiene estos métodos.



| Método                            | Descripción                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienummedia-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienummedia-next.md)   | Obtiene el siguiente número especificado de elementos de la secuencia de enumeración.<br/>                 |
| [**Restablecer**](ienummedia-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienummedia-skip.md)   | Omite el siguiente número especificado de elementos en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

