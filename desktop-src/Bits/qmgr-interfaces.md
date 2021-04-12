---
title: Interfaces QMGR
description: Use las siguientes interfaces de administrador de cola (QMGR) para descargar archivos y supervisar trabajos en la cola de descarga.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268317"
---
# <a name="qmgr-interfaces"></a>Interfaces QMGR

\[Las interfaces del administrador de colas (QMGR) están disponibles para su uso en los sistemas operativos especificados en la sección requisitos de un tema. Podrán modificarse o no estar disponibles en versiones posteriores. En su lugar, use las [interfaces de bits](bits-interfaces.md).\]

Use las siguientes interfaces de administrador de cola (QMGR) para descargar archivos y supervisar trabajos en la cola de descarga.



| Interfaz                                                                 | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implemente para recibir una notificación cuando se produzcan eventos.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Use para administrar el grupo. Por ejemplo, agregue un trabajo al grupo, establezca las propiedades del grupo e inicie y detenga el grupo en la cola de descarga.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Use para agregar archivos al trabajo y recuperar el estado del trabajo.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Use para crear un nuevo grupo, recuperar un grupo existente o enumerar todos los grupos de la cola.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Use para recuperar una lista de grupos en la cola de descarga.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Use para recuperar una lista de trabajos del grupo.<br/>                                                                                                       |



 

 

 





