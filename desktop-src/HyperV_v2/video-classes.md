---
description: Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Clases de vídeo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a1880a37b6d71ef561cf702cce27a4b86f091701fcadbec59797343440238d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075255"
---
# <a name="video-classes"></a>Clases de vídeo

Todas las máquinas virtuales reflejan la presencia de un controlador de vídeo S3 emulado y un controlador de vídeo sintético y acelerado.

Cada controlador de pantalla tiene un objeto principal de vídeo asociado. Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento.

Hay una conexión de terminal para cada sesión remota activa conectada a una máquina virtual.

Las siguientes son clases WMI de virtualización relacionadas con el vídeo.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                  | Descripción                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | Representa el estado del controlador S3 emulado que está presente en cada configuración de máquina virtual.<br/>       |
| [**Msvm \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)<br/> | Representa el estado del controlador de pantalla sintético que está presente en cada configuración de máquina virtual.<br/> |
| [**Msvm \_ SystemTerminalConnection**](msvm-systemterminalconnection.md)<br/>     | Asocia una máquina virtual a una conexión de terminal.<br/>                                                        |
| [**TerminalConnection de Msvm \_**](msvm-terminalconnection.md)<br/>                 | Indica el estado de una sesión remota activa que interactúa con una máquina virtual.<br/>                             |
| [**Msvm \_ VideoHead**](msvm-videohead.md)<br/>                                   | Describe la superficie de dibujo principal en un controlador de pantalla.<br/>                                                  |
| [**Msvm \_ VideoHeadOnController**](msvm-videoheadoncontroller.md)<br/>           | Asocia un responsable de vídeo al controlador de vídeo que lo incluye.<br/>                                             |



 

 

 




