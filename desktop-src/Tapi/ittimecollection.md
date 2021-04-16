---
description: La interfaz ITTimeCollection es una interfaz específica del proveedor para el objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaz ITTimeCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690234"
---
# <a name="ittimecollection-interface"></a>Interfaz ITTimeCollection

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITTimeCollection** es una interfaz específica del proveedor para el objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP). Esta interfaz permite el acceso a las interfaces de [**ITTime**](ittime.md) por índice y también habilita la creación y la eliminación de componentes de hora. El método [**ITSdp:: get \_ TimeCollection**](itsdp-get-timecollection.md) crea la interfaz **ITTimeCollection** .

## <a name="members"></a>Miembros

La interfaz **ITTimeCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTimeCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITTimeCollection** tiene estos métodos.



| Método                                                           | Descripción                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**A**](ittimecollection-create.md)                        | Crea un componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**Elimínelos**](ittimecollection-delete.md)                        | Elimina un componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**obtener \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Devuelve un enumerador para la colección.<br/>                                                                  |
| [**obtener \_ recuento**](ittimecollection-get-count.md)                 | Obtiene el número de elementos de la colección.<br/>                                                                        |
| [**obtener \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Devuelve la interfaz de enumeración [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).<br/> |
| [**obtener \_ elemento**](ittimecollection-get-item.md)                   | Dado un índice, devuelve un elemento de la colección.<br/>                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

