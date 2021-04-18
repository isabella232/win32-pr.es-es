---
description: La interfaz IStas proporciona los métodos que se usan para conectar un NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red. Esta interfaz genera estadísticas sin fotogramas.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaz IStas (Netmon. h)
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
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687000"
---
# <a name="istats-interface"></a>Interfaz IStas

La interfaz **istas** proporciona los métodos que se usan para conectar un NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red. Esta interfaz genera estadísticas sin fotogramas.

## <a name="members"></a>Miembros

La interfaz **istas** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Los **ISTA** también tienen estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **istas** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configuración**](istats-configure.md)                                 | Configura el desencadenador, la coincidencia de patrón y el tamaño del búfer del archivo de captura.<br/>                                                                    |
| [**Conectar**](istats-connect.md)                                     | Conecta el NPP a la red.<br/>                                                                                                               |
| [**Desconectar**](istats-disconnect.md)                               | Desconecta el NPP de la red.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Recupera información de la [*sesión*](s.md) y de la [*estación*](s.md) sobre la captura actual.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Extrae la hora, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.<br/>                                                |
| [**Pausar**](istats-pause.md)                                         | Detiene temporalmente la captura actual.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Recupera el estado de NPP.<br/>                                                                                                               |
| [**Reanudar**](istats-resume.md)                                       | Reinicia una captura en pausa.<br/>                                                                                                                     |
| [**Start**](istats-start.md)                                         | Inicia la captura.<br/>                                                                                                                            |
| [**Stop**](istats-stop.md)                                           | Detiene la captura actual.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

