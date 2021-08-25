---
description: El MSP de IPConf implementa la interfaz IMulticastControl y solo está disponible en objetos de llamada de multidifusión.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaz IMulticastControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7469ca26a49bc25b36ae87727a1fdcf324bcf54e8a253805ed56f252c7f062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905955"
---
# <a name="imulticastcontrol-interface"></a>Interfaz IMulticastControl

\[**IMulticastControl** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El MSP de IPConf implementa la interfaz **IMulticastControl** y solo está disponible en objetos de llamada de multidifusión. Esta interfaz expone métodos que permiten la creación y manipulación de terminales que pueden comunicarse entre clientes H323 y SDP. La **interfaz IMulticastControl controla** el modo de bucle atrás de multidifusión.

En el modo MM NO LOOPBACK, el bucle de multidifusión está deshabilitado, lo que significa que dos aplicaciones del mismo equipo que se unen al mismo grupo de multidifusión recibirán los paquetes de los \_ \_ demás. Este modo tiene el mejor rendimiento si siempre hay una sola aplicación que se une al grupo de multidifusión en la máquina. El \_ modo MM NO \_ LOOPBACK es el modo predeterminado.

El modo \_ MM FULL \_ LOOPBACK solo es bueno para las pruebas. Todos los paquetes enviados también se recorren en bucle. Esto se puede usar para probar si los dispositivos funcionan.

El modo MM SELECTIVE LOOPBACK se usa para permitir que varias \_ aplicaciones de un equipo se \_ unan al mismo grupo de multidifusión. Los paquetes se recorren en bucle desde la pila y cada sesión RTP es responsable de filtrar los paquetes no deseados.

## <a name="members"></a>Miembros

La **interfaz IMulticastControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMulticastControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMulticastControl** tiene estos métodos.



| Método                                                          | Descripción                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Obtiene el modo de bucle recuperación de multidifusión.<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Establece el modo de bucle atrás de multidifusión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

