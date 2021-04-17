---
description: Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecuten como usuario estándar.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Desarrollo de aplicaciones que requieren privilegios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652897"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Desarrollo de aplicaciones que requieren privilegios de administrador

Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecuten como usuario estándar.

Hay varios modelos para lograr esto.



| Tema                                                                | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de tareas elevado](elevated-task-model.md)                       | Una aplicación que se ejecuta como usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.                                                                     |
| [Modelo de servicio del sistema operativo](operating-system-service-model.md) | Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **sistema** mediante la [llamada a procedimiento remoto](/windows/desktop/Rpc/rpc-start-page) (RPC).                                              |
| [Modelo de agente de administrador](administrator-broker-model.md)         | La aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.                                                          |
| [Modelo de objetos COM de administrador](administrator-com-object-model.md) | Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto de [modelo de objetos de componente](/windows/desktop/com/component-object-model--com--portal) elevado. |



 

 

 
