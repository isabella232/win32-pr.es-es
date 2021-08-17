---
description: La interfaz ITTimeCollection es una interfaz específica del proveedor para el objeto de blob de conferencia Del Protocolo de descriptor de sesión (SDP).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaz ITTimeCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d086dcf0df7fb4d55552c734798244209fc3e9f52a2f2462693f6aaad7110347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762299"
---
# <a name="ittimecollection-interface"></a>Interfaz ITTimeCollection

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITTimeCollection** es una interfaz específica del proveedor para el objeto de blob de conferencia Del Protocolo de descriptor de sesión (SDP). Esta interfaz permite el acceso a las interfaces [**ITTime**](ittime.md) por índice y también permite la creación y eliminación de componentes de tiempo. El [**método ITSdp::get \_ TimeCollection**](itsdp-get-timecollection.md) crea la **interfaz ITTimeCollection.**

## <a name="members"></a>Miembros

La **interfaz ITTimeCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITTimeCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITTimeCollection** tiene estos métodos.



| Método                                                           | Descripción                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Crear**](ittimecollection-create.md)                        | Crea un [**componente ITTime.**](ittime.md)<br/>                                                             |
| [**Eliminar**](ittimecollection-delete.md)                        | Elimina un componente [**ITTime.**](ittime.md)<br/>                                                             |
| [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Devuelve un enumerador para la colección.<br/>                                                                  |
| [**get \_ Count**](ittimecollection-get-count.md)                 | Obtiene el número de elementos de la colección.<br/>                                                                        |
| [**get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Devuelve la [**interfaz de enumeración IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).<br/> |
| [**get \_ Item**](ittimecollection-get-item.md)                   | Dado un índice, devuelve un elemento de la colección.<br/>                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

