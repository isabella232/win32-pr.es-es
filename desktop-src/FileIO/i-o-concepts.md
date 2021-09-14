---
description: Describe los conceptos básicos de E/S.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Conceptos de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069924"
---
# <a name="io-concepts"></a>Conceptos de E/S

En esta sección se describen los siguientes conceptos de E/S.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Almacenamiento en búfer de archivo](file-buffering.md)<br/>                                     | Describe las consideraciones para el control de la aplicación del almacenamiento en búfer de archivos, también conocido como entrada/salida de archivos no almacenados en búfer (E/S).<br/>                                    |
| [Almacenamiento en caché de archivos](file-caching.md)<br/>                                         | Windows almacena en caché los datos de archivo que se leen de los discos y se escriben en los discos.<br/>                                                                                   |
| [E/S sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)<br/> | Hay dos tipos de sincronización de entrada/salida (E/S): E/S sincrónica y E/S asincrónica. La E/S asincrónica también se conoce como E/S superpuesta.<br/> |
| [Cancelación de operaciones de E/S pendientes](canceling-pending-i-o-operations.md)<br/> | Permitir a los usuarios cancelar solicitudes de E/S lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.<br/>                             |
| [E/S que se puede alertar](alertable-i-o.md)<br/>                                       | E/S que admite alertas es el método por el que los subprocesos de aplicación procesan solicitudes de E/S asincrónicas solo cuando se encuentran en un estado de alerta.<br/>                     |
| [Puertos de finalización de E/S](i-o-completion-ports.md)<br/>                         | Los puertos de finalización de E/S proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de E/S asincrónicas en un sistema de varios procesadores.<br/>                  |



 

 

 




