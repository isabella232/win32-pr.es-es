---
description: La interfaz IDelaydC proporciona los métodos que se usan para conectarse a la red, capturar el tráfico de red a un archivo de captura, recuperar estadísticas y desconectarse de la red.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interfaz IDelaydC (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074135"
---
# <a name="idelaydc-interface"></a>Interfaz IDelaydC

La **interfaz IDelaydC** proporciona los métodos que se usan para conectarse a la red, capturar el tráfico de red a un archivo de captura, recuperar estadísticas y desconectarse de la red.

Esta interfaz captura fotogramas del flujo de datos de red y, a continuación, copia los fotogramas en un archivo de captura. Esta interfaz la usan las aplicaciones Monitor de red y NPP. Para recibir los datos de red, la NIC de destino debe admitir el modo promiscuo.

## <a name="members"></a>Members

La **interfaz IDelaydC** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDelaydC** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDelaydC** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configuración**](idelaydc-configure.md)                                 | Envía la información de configuración utilizada para una captura.<br/>                                                                                        |
| [**Conexión**](idelaydc-connect.md)                                     | Conecta el NPP a la red.<br/>                                                                                                             |
| [**Desconectar**](idelaydc-disconnect.md)                               | Desconecta el NPP de la red.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o en pausa.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Recupera la [*información de*](s.md) la sesión y [*la estación*](s.md) para la captura actual.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Extrae el tiempo, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.<br/>                                              |
| [**Pausar**](idelaydc-pause.md)                                         | Detiene temporalmente la captura actual.<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Recupera el estado del NPP.<br/>                                                                                                             |
| [**Reanudar**](idelaydc-resume.md)                                       | Reanuda una captura en pausa.<br/>                                                                                                                    |
| [**Empezar**](idelaydc-start.md)                                         | Inicia una captura y crea el [*archivo de captura*](c.md).<br/>                                                           |
| [**Stop**](idelaydc-stop.md)                                           | Detiene la captura actual y cierra el [*archivo de captura*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

