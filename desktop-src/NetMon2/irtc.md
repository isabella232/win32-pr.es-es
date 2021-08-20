---
description: La interfaz IRTC proporciona los métodos que se usan para conectar el NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interfaz IRTC (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132934"
---
# <a name="irtc-interface"></a>Interfaz IRTC

La **interfaz IRTC** proporciona los métodos que se usan para conectar el NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red. **IRTC** obtiene una interfaz a los puntos de entrada solo locales, que son necesarios para participar en la captura en tiempo real. Esta interfaz incluye un método que entrega una devolución de llamada al NPP.

## <a name="members"></a>Miembros

La **interfaz IRTC** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRTC** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRTC** tiene estos métodos.



| Método                                                              | Descripción                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](irtc-configure.md)                                 | Establece el desencadenador, la coincidencia de patrones y el tamaño del búfer de la captura.<br/>                                                                             |
| [**Conectar**](irtc-connect.md)                                     | Conecta el NPP a la red.<br/>                                                                                                             |
| [**Desconectar**](irtc-disconnect.md)                               | Desconecta el NPP de la red.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o en pausa.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Recupera la [*información de*](s.md) la sesión y [*la estación*](s.md) para la captura actual.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Extrae el tiempo, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.<br/>                                              |
| [**Pausar**](irtc-pause.md)                                         | Detiene temporalmente la captura actual.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Recupera una lista de todos los equipos de una subred que usan Monitor de red para capturar datos de red.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Recupera el estado del NPP.<br/>                                                                                                             |
| [**Reanudar**](irtc-resume.md)                                       | Reinicia una captura en pausa.<br/>                                                                                                                   |
| [**Inicio**](irtc-start.md)                                         | Inicia una captura.<br/>                                                                                                                            |
| [**Stop**](irtc-stop.md)                                           | Detiene la captura actual.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

