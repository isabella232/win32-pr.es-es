---
description: La interfaz ITAttributeList proporciona métodos para obtener y establecer atributos no interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaz ITAttributeList (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8dd0ac143791a09eedbd3fe575dcecb894a1fb6dbb218c8ecfdcadf60ebd60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762431"
---
# <a name="itattributelist-interface"></a>ItAttributeList (interfaz)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITAttributeList** proporciona métodos para obtener y establecer atributos no interpretados. Con respecto a la posición de las cadenas de atributo en un paquete del Protocolo de descriptor de sesión (SDP, consulte RFC 2327), los métodos asumen que todas las cadenas de atributo existen justo antes de que se especifiquen los atributos multimedia y después de todos los atributos comunes. La **interfaz ITAttributeList** se crea mediante una llamada **a QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Miembros

La **interfaz ITAttributeList** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITAttributeList también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITAttributeList** tiene estos métodos.



| Método                                                          | Descripción                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Añadir**](itattributelist-add.md)                              | Agrega el atributo en el índice especificado.<br/>   |
| [**Eliminar**](itattributelist-delete.md)                        | Elimina el atributo en el índice especificado.<br/> |
| [**get \_ AttributeList**](itattributelist-get-attributelist.md) | Obtiene la lista de atributos.<br/>                 |
| [**get \_ Count**](itattributelist-get-count.md)                 | Obtiene el número de atributos.<br/>               |
| [**get \_ Item**](itattributelist-get-item.md)                   | Obtiene el atributo especificado por el índice.<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | Establece la lista de atributos.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

