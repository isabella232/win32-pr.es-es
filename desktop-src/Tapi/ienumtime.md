---
description: La interfaz IEnumTime proporciona métodos de enumeración com estándar para la interfaz ITTime. El método ITTimeCollection::get \_ EnumerationIf devuelve un puntero a IEnumTime.
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaz IEnumTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068758"
---
# <a name="ienumtime-interface"></a>IEnumTime (interfaz)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IEnumTime proporciona métodos** de enumeración com estándar para la [**interfaz ITTime.**](ittime.md) El [**método ITTimeCollection::get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) devuelve un puntero a **IEnumTime**.

## <a name="members"></a>Members

La **interfaz IEnumTime** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumTime también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumTime** tiene estos métodos.



| Método                           | Descripción                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumtime-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumtime-next.md)   | Obtiene el siguiente número especificado de elementos de la secuencia de enumeración.<br/>                 |
| [**Reset**](ienumtime-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Saltar**](ienumtime-skip.md)   | Omite el siguiente número especificado de elementos en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

