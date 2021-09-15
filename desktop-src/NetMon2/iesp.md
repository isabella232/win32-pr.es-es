---
description: La interfaz IESP proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaz IESP (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476716"
---
# <a name="iesp-interface"></a>Interfaz IESP

La **interfaz IESP** proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red. Esta interfaz se usa principalmente cuando necesita recopilar [*estadísticas*](c.md) de conversación de red en un formato de archivo ESP propietario.

## <a name="members"></a>Members

La **interfaz IESP** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IESP** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IESP** tiene estos métodos.



| Método                                          | Descripción                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configuración**](iesp-configure.md)             | Envía información de configuración para una captura<br/>                                                                         |
| [**Conexión**](iesp-connect.md)                 | Conecta el NPP a la red.<br/>                                                                                        |
| [**Desconectar**](iesp-disconnect.md)           | Desconecta el NPP de la red.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o en pausa.<br/> |
| [**Pausar**](iesp-pause.md)                     | Detiene temporalmente la captura actual.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Recupera el estado del NPP.<br/>                                                                                        |
| [**Reanudar**](iesp-resume.md)                   | Reanuda una captura en pausa.<br/>                                                                                               |
| [**Empezar**](iesp-start.md)                     | Inicia la captura y crea el archivo de captura.<br/>                                                                        |
| [**Stop**](iesp-stop.md)                       | Detiene la captura actual.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

