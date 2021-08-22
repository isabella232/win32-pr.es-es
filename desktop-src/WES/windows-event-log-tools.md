---
title: Windows Herramientas del registro de eventos
description: Windows El registro de eventos proporciona las siguientes herramientas que se usan para compilar el proveedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7a0aef85e85e096381b65d41458f1cb955ba9701452498d21c45ff25cb3058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587262"
---
# <a name="windows-event-log-tools"></a>Windows Herramientas del registro de eventos

Windows El registro de eventos proporciona las siguientes herramientas que se usan para compilar el proveedor.



| Herramienta                                                           | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md)  | Una utilidad de línea de comandos que se usa para compilar manifiestos de instrumentación y archivos de texto de mensaje. |
| WevtUtil.exe                                                   | Una utilidad de línea de comandos que se usa principalmente para registrar el proveedor en el equipo. También puede usarlo para obtener información de metadatos sobre el proveedor, sus eventos y los canales en los que registra eventos, y para consultar eventos de un canal o archivo de registro. La WevtUtil.exe se incluye en %windir% \\ System32. Para obtener información de uso, escriba "wevtutil /?" en un símbolo del sistema.<br/> Este comando se limita a los miembros del grupo Administradores y debe ejecutarse con privilegios elevados.|
