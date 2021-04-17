---
title: Herramientas del registro de eventos de Windows
description: El registro de eventos de Windows proporciona las siguientes herramientas que se usan para compilar el proveedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104420492"
---
# <a name="windows-event-log-tools"></a>Herramientas del registro de eventos de Windows

El registro de eventos de Windows proporciona las siguientes herramientas que se usan para compilar el proveedor.



| Herramienta                                                           | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md)  | Utilidad de línea de comandos que se usa para compilar manifiestos de instrumentación y archivos de texto de mensaje. |
| WevtUtil.exe                                                   | Utilidad de línea de comandos que se usa principalmente para registrar el proveedor en el equipo. También se puede utilizar para obtener información de metadatos sobre el proveedor, sus eventos y los canales en los que se registran los eventos, y para consultar los eventos de un canal o un archivo de registro. La herramienta de WevtUtil.exe se incluye en% WINDIR% \\ system32. Para obtener información de uso, escriba "wevtutil/?" en un símbolo del sistema.<br/> Este comando está limitado a los miembros del grupo administradores y debe ejecutarse con privilegios elevados.|
