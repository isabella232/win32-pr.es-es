---
description: 'La interfaz IEnumTime proporciona métodos de enumeración estándar de COM para la interfaz ITTime. El método ITTimeCollection:: get \_ EnumerationIf devuelve un puntero a IEnumTime.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaz IEnumTime (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680322"
---
# <a name="ienumtime-interface"></a>Interfaz IEnumTime

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **IEnumTime** proporciona métodos de enumeración estándar de com para la interfaz [**ITTime**](ittime.md) . El método [**ITTimeCollection:: get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) devuelve un puntero a **IEnumTime**.

## <a name="members"></a>Miembros

La interfaz **IEnumTime** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumTime** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumTime** tiene estos métodos.



| Método                           | Descripción                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumtime-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumtime-next.md)   | Obtiene el siguiente número de elementos especificado en la secuencia de enumeración.<br/>                 |
| [**Reset**](ienumtime-reset.md) | Se restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumtime-skip.md)   | Omite el siguiente número de elementos especificado en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

