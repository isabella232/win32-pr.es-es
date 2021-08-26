---
description: Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecute como un usuario estándar.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Desarrollo de aplicaciones que requieren privilegios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dc8ea112cfec6297cf7c11a044e62695a24e93d7eb0b13a773d40acd6c6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994435"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Desarrollo de aplicaciones que requieren privilegios de administrador

Es posible desarrollar una aplicación que realice operaciones que requieran privilegios de administrador y que se ejecute como un usuario estándar.

Hay varios modelos para lograrlo.



| Tema                                                                | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de tareas con privilegios elevados](elevated-task-model.md)                       | Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.                                                                     |
| [Modelo de servicio de sistema operativo](operating-system-service-model.md) | Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **SYSTEM** mediante la llamada a [procedimiento remoto](/windows/desktop/Rpc/rpc-start-page) (RPC).                                              |
| [Modelo de Agente de administrador](administrator-broker-model.md)         | La aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro se ejecuta con privilegios de administrador.                                                          |
| [Modelo de objetos COM de administrador](administrator-com-object-model.md) | Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto De modelo de [objetos componentes con privilegios](/windows/desktop/com/component-object-model--com--portal) elevados. |



 

 

 
