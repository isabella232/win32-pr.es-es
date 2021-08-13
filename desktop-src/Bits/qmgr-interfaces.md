---
title: QMGR Interfaces
description: Use las siguientes interfaces del Administrador de colas (QMGR) para descargar archivos y supervisar trabajos dentro de la cola de descarga.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679999"
---
# <a name="qmgr-interfaces"></a>QMGR Interfaces

\[Las interfaces de Queue Manager (QMGR) están disponibles para su uso en los sistemas operativos especificados en la sección Requisitos de un tema. Podrán modificarse o no estar disponibles en versiones posteriores. En su lugar, use [las interfaces bits](bits-interfaces.md).\]

Use las siguientes interfaces del Administrador de colas (QMGR) para descargar archivos y supervisar trabajos dentro de la cola de descarga.



| Interfaz                                                                 | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implemente para recibir notificaciones cuando se produzcan eventos.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Use para administrar el grupo. Por ejemplo, agregue un trabajo al grupo, establezca las propiedades del grupo e inicie y detenga el grupo en la cola de descarga.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Use para agregar archivos al trabajo y recuperar el estado del trabajo.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Use para crear un nuevo grupo, recuperar un grupo existente o enumerar todos los grupos de la cola.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Use para recuperar una lista de grupos en la cola de descarga.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Use para recuperar una lista de trabajos del grupo.<br/>                                                                                                       |



 

 

 





