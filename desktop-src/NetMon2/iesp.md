---
description: La interfaz IESP proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaz IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154146"
---
# <a name="iesp-interface"></a>Interfaz IESP

La interfaz **iesp** proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red. Esta interfaz se utiliza principalmente cuando necesita recopilar estadísticas de [*conversación*](c.md) de red en un formato de archivo ESP propietario.

## <a name="members"></a>Miembros

La interfaz **iesp** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Iesp** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **iesp** tiene estos métodos.



| Método                                          | Descripción                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configuración**](iesp-configure.md)             | Envía la información de configuración de una captura.<br/>                                                                         |
| [**Conectar**](iesp-connect.md)                 | Conecta el NPP a la red.<br/>                                                                                        |
| [**Desconectar**](iesp-disconnect.md)           | Desconecta el NPP de la red.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.<br/> |
| [**Pausar**](iesp-pause.md)                     | Detiene temporalmente la captura actual.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Recupera el estado de NPP.<br/>                                                                                        |
| [**Reanudar**](iesp-resume.md)                   | Reanuda una captura en pausa.<br/>                                                                                               |
| [**Start**](iesp-start.md)                     | Inicia la captura y crea el archivo de captura.<br/>                                                                        |
| [**Stop**](iesp-stop.md)                       | Detiene la captura actual.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

