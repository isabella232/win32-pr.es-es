---
description: IPConf MSP implementa la interfaz IMulticastControl y solo está disponible en los objetos de llamada de multidifusión.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaz IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690785"
---
# <a name="imulticastcontrol-interface"></a>Interfaz IMulticastControl

\[**IMulticastControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

IPConf MSP implementa la interfaz **IMulticastControl** y solo está disponible en los objetos de llamada de multidifusión. Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP. La interfaz **IMulticastControl** controla el modo de bucle invertido de multidifusión.

En el \_ modo mm no \_ loopback, se deshabilita el bucle invertido de multidifusión, lo que significa que dos aplicaciones en el mismo equipo que se unen al mismo grupo de multidifusión obtendrán los paquetes de los demás. Este modo tiene el mejor rendimiento si siempre hay una aplicación que se une al grupo de multidifusión en el equipo. MM \_ no hay \_ modo de bucle invertido es el modo predeterminado.

El \_ \_ modo de bucle invertido completo de mm solo es adecuado para pruebas. También se recorren en bucle todos los paquetes enviados. Se puede usar para comprobar si los dispositivos funcionan.

El \_ modo bucle selectivo de mm \_ se usa para permitir que varias aplicaciones de un equipo se unan al mismo grupo de multidifusión. Los paquetes se recorren en bucle desde la pila y cada sesión de RTP es responsable de filtrar los paquetes no deseados.

## <a name="members"></a>Miembros

La interfaz **IMulticastControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMulticastControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMulticastControl** tiene estos métodos.



| Método                                                          | Descripción                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**obtener \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Obtiene el modo de bucle invertido de multidifusión.<br/> |
| [**Put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Establece el modo de bucle invertido de multidifusión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

