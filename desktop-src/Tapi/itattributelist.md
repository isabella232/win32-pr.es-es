---
description: La interfaz ITAttributeList proporciona métodos para obtener y establecer los atributos no interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaz ITAttributeList (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690925"
---
# <a name="itattributelist-interface"></a>Interfaz ITAttributeList

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITAttributeList** proporciona métodos para obtener y establecer los atributos no interpretados. En cuanto a la posición de las cadenas de atributo en un paquete de protocolo de descriptor de sesión (SDP, vea RFC 2327), los métodos suponen que todas las cadenas de atributo existen justo antes de que se especifiquen los atributos multimedia y después de todos los atributos comunes. La interfaz **ITAttributeList** se crea llamando a **QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Miembros

La interfaz **ITAttributeList** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITAttributeList** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITAttributeList** tiene estos métodos.



| Método                                                          | Descripción                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Agréguela**](itattributelist-add.md)                              | Agrega el atributo en el índice especificado.<br/>   |
| [**Elimínelos**](itattributelist-delete.md)                        | Elimina el atributo en el índice especificado<br/> |
| [**obtener \_ AttributeList**](itattributelist-get-attributelist.md) | Obtiene la lista de atributos.<br/>                 |
| [**obtener \_ recuento**](itattributelist-get-count.md)                 | Obtiene el número de atributos.<br/>               |
| [**obtener \_ elemento**](itattributelist-get-item.md)                   | Obtiene el atributo especificado por el índice.<br/>   |
| [**Put \_ AttributeList**](itattributelist-put-attributelist.md) | Establece la lista de atributos.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

