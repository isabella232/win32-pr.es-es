---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivos MCI, controlador MCIAVI
- Comandos MCI, controlador MCIAVI
- Controlador MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486898"
---
# <a name="mciavi"></a>MCIAVI

Un archivo AVI puede contener más de dos secuencias, por ejemplo, una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés. La aplicación puede utilizar una secuencia independientemente de las demás secuencias del archivo.

El tipo de dispositivo **DigitalVideo** controla los archivos de vídeo. Para obtener una lista de los comandos MCI reconocidos por los dispositivos de vídeo digital, consulte [conjunto de comandos de vídeo digital](digital-video-command-set.md).

El controlador MCIAVI reproduce secuencias de vídeo y otros flujos de datos bajo el control de los comandos MCI. Los flujos de datos pueden contener imágenes, audio y paletas. Los datos de imagen pueden constar de imágenes con paletas de colores o información de color verdadero.

El audio se sincroniza con el vídeo dentro de un trigésima de segundo. Sin embargo, si el hardware de audio no está disponible, el controlador solo reproduce la secuencia de vídeo. El controlador MCIAVI puede quitar fotogramas de vídeo, si es necesario, para reproducir un flujo sin interrupción de audio.

La aplicación puede usar los servicios de clase de ventana MCIWnd en lugar de la interfaz de comandos MCI para controlar cualquier controlador MCI. Esta clase de ventana administra muchos de los detalles de la administración de la ventana que admite el dispositivo MCI y simplifica la programación necesaria para enviar los comandos MCI. La aplicación puede usar los servicios de biblioteca MCIWnd directamente para controlar el dispositivo MCI, o bien puede tener MCIWnd mostrar una barra de herramientas, una barra de desplazamiento y menús que permitan al usuario controlar el dispositivo. Para obtener más información sobre la clase de ventana MCIWnd, consulte [clase de ventana MCIWnd](mciwnd-window-class.md).

 

 




