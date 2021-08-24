---
description: La interfaz ITMediaCollection proporciona acceso al conjunto de información multimedia en una descripción de conferencia de SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interfaz ITMediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2425ae89f376d5cb2d7cc23e70abd33f87750d3d1b5343a17c8ecb05d7de760d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034615"
---
# <a name="itmediacollection-interface"></a>Interfaz ITMediaCollection

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITMediaCollection** proporciona acceso al conjunto de información multimedia en una descripción de conferencia de SDP (RFC 2327). Cada descripción de los medios del SDP se describe mediante una [**interfaz ITMedia.**](itmedia.md) **ITMediaCollection permite** la manipulación del conjunto de **información itmedia** para el SDP, lo que incluye:

-   Permite el acceso multimedia por índice.
-   Habilita la creación y eliminación de medios.

El [**método ITSdp::get \_ MediaCollection**](itsdp-get-mediacollection.md) crea la **interfaz ITMediaCollection.**

## <a name="members"></a>Miembros

La **interfaz ITMediaCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMediaCollection también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITMediaCollection** tiene estos métodos.



| Método                                                            | Descripción                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Crear**](itmediacollection-create.md)                        | Crea un nuevo medio con propiedades predeterminadas y lo devuelve.<br/> |
| [**Eliminar**](itmediacollection-delete.md)                        | Elimina el medio correspondiente al índice especificado.<br/>     |
| [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Devuelve un enumerador para la colección.<br/>                   |
| [**get \_ Count**](itmediacollection-get-count.md)                 | Obtiene el número de medios de la sesión.<br/>                    |
| [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Obtiene el puntero a la interfaz de enumeración.<br/>                      |
| [**get \_ Item**](itmediacollection-get-item.md)                   | Devuelve el medio correspondiente al índice especificado.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

