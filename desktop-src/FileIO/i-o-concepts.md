---
description: Describe los conceptos básicos de e/s.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Conceptos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688461"
---
# <a name="io-concepts"></a>Conceptos de e/s

En esta sección se describen los siguientes conceptos de e/s.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Almacenamiento en búfer de archivo](file-buffering.md)<br/>                                     | Describe las consideraciones para el control de aplicaciones del almacenamiento en búfer de archivos, también conocido como entrada/salida (e/s) de archivo no almacenado en búfer.<br/>                                    |
| [Almacenamiento en caché de archivos](file-caching.md)<br/>                                         | Windows almacena en caché los datos de archivos que se leen de los discos y se escriben en los discos.<br/>                                                                                   |
| [E/s sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)<br/> | Hay dos tipos de sincronización de entrada/salida (e/s): e/s sincrónica y de e/s asincrónica. La e/s asincrónica también se conoce como e/s superpuesta.<br/> |
| [Cancelar operaciones de e/s pendientes](canceling-pending-i-o-operations.md)<br/> | Permitir a los usuarios cancelar las solicitudes de e/s que son lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.<br/>                             |
| [E/s de alertas](alertable-i-o.md)<br/>                                       | La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.<br/>                     |
| [Puertos de finalización de e/s](i-o-completion-ports.md)<br/>                         | Los puertos de finalización de e/s proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de e/s asincrónicas en un sistema de varios procesadores.<br/>                  |



 

 

 




