---
title: Directrices para tareas en segundo plano en Servicios de Escritorio remoto
description: Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecuten en un entorno Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consumen muchos recursos.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249968"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Directrices para tareas en segundo plano en Servicios de Escritorio remoto

Las tareas en segundo plano (tareas realizadas cuando el bucle de mensajes de una aplicación está inactivo) proporcionan un mecanismo para controlar las tareas de prioridad baja en un entorno de usuario único. En un Servicios de Escritorio remoto, sin embargo, la tarea en segundo plano de un usuario compite por los ciclos de CPU con las tareas en primer plano de otro usuario. Cuando varios usuarios ejecutan tareas en primer plano y en segundo plano, las demandas de CPU son mucho mayores que cuando todos los usuarios solo ejecutan tareas en primer plano. Para maximizar la disponibilidad de la CPU para todos los usuarios, deshabilite las tareas en segundo plano cuando se ejecuten en un entorno Servicios de Escritorio remoto o cree tareas en segundo plano eficaces que no consumen muchos recursos.

Para obtener más información, vea [Detección de la Servicios de Escritorio remoto entorno](detecting-the-terminal-services-environment.md). Después de detectar el Servicios de Escritorio remoto, puede deshabilitar o volver a configurar las tareas en segundo plano para la aplicación con el mismo conjunto de API que usó para administrar las tareas.

 

 




