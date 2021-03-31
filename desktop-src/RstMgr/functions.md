---
title: Funciones del administrador de reinicio
description: La API del administrador de reinicio usa las funciones que se identifican en la tabla siguiente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Admin. de reinicio del administrador, referencia, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903385"
---
# <a name="restart-manager-functions"></a>Funciones del administrador de reinicio

La API del administrador de reinicio usa las funciones que se identifican en la tabla siguiente.



| Función                                           | Descripción                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifica las acciones de cierre o reinicio.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Inicia una nueva sesión del administrador de reinicio.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Une el proceso de una aplicación a una sesión del administrador de reinicio existente.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Finaliza la sesión del administrador de reinicio.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registra los recursos, como nombres de archivo, nombres cortos de servicio o estructuras de [**\_ \_ proceso único de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , en una sesión del administrador de reinicio.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Lo usan los instaladores para obtener una lista de todas las aplicaciones afectadas por los recursos registrados y su estado actual.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Consulta el estado de cierre y reinicio de las modificaciones que ya se han aplicado.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Inicia el cierre de aplicaciones y servicios.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Quita las modificaciones de apagado y reinicio que ya se han aplicado.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Reinicia las aplicaciones y los servicios que se han cerrado con la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) y que se han registrado para reiniciarse con **RegisterApplicationRestart**. |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Cancela la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actual.                                                            |



 

 

 




