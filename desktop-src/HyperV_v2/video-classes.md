---
description: Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Clases de vídeo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498023"
---
# <a name="video-classes"></a>Clases de vídeo

Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.

Cada controlador de pantalla tiene un objeto de encabezado de vídeo asociado a él. Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento.

Existe una conexión de terminal para todas las sesiones remotas activas conectadas a una máquina virtual.

A continuación se enumeran las clases WMI de virtualización relacionadas con el vídeo.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                  | Descripción                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual.<br/>       |
| [**MSVM \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)<br/> | Representa el estado del controlador de pantalla sintético presente en cada configuración de máquina virtual.<br/> |
| [**MSVM \_ SystemTerminalConnection**](msvm-systemterminalconnection.md)<br/>     | Asocia una máquina virtual a una conexión de terminal.<br/>                                                        |
| [**MSVM \_ TerminalConnection**](msvm-terminalconnection.md)<br/>                 | Indica el estado de una sesión remota activa que interactúa con una máquina virtual.<br/>                             |
| [**Videopartida MSVM \_**](msvm-videohead.md)<br/>                                   | Describe la superficie de dibujo principal en un controlador de pantalla.<br/>                                                  |
| [**MSVM \_ VideoHeadOnController**](msvm-videoheadoncontroller.md)<br/>           | Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.<br/>                                             |



 

 

 




