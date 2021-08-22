---
description: La interfaz IStats proporciona los métodos que se usan para conectar un NPP a la red, capturar tráfico de red, recuperar estadísticas y desconectar el NPP de la red. Esta interfaz genera estadísticas sin fotogramas.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaz IStats (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27a43f8ea2902af7e2847e032da18543ffdbb228c2aa3e49fde63ce7cd727512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495015"
---
# <a name="istats-interface"></a>Interfaz IStats

La **interfaz IStats** proporciona los métodos que se usan para conectar un NPP a la red, capturar tráfico de red, recuperar estadísticas y desconectar el NPP de la red. Esta interfaz genera estadísticas sin fotogramas.

## <a name="members"></a>Miembros

La **interfaz IStats** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IStats** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IStats** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](istats-configure.md)                                 | Configura el desencadenador, la coincidencia de patrones y el tamaño del búfer del archivo de captura.<br/>                                                                    |
| [**Conectar**](istats-connect.md)                                     | Conecta el NPP a la red.<br/>                                                                                                               |
| [**Desconectar**](istats-disconnect.md)                               | Desconecta el NPP de la red.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o en pausa.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Recupera la [*información de*](s.md) la sesión y [*la estación*](s.md) sobre la captura actual.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Extrae el tiempo, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.<br/>                                                |
| [**Pausar**](istats-pause.md)                                         | Detiene temporalmente la captura actual.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Recupera el estado del NPP.<br/>                                                                                                               |
| [**Reanudar**](istats-resume.md)                                       | Reinicia una captura en pausa.<br/>                                                                                                                     |
| [**Inicio**](istats-start.md)                                         | Inicia la captura.<br/>                                                                                                                            |
| [**Stop**](istats-stop.md)                                           | Detiene la captura actual.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

