---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivos MCI, controlador MCIAVI
- Comandos de MCI, controlador MCIAVI
- Controlador MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245834"
---
# <a name="mciavi"></a>MCIAVI

Un archivo AVI puede contener más de dos secuencias, por ejemplo, una secuencia de vídeo, un inglés y un francés. La aplicación puede usar una secuencia independientemente de las demás secuencias del archivo.

El **tipo de dispositivo digitalvideo** controla los archivos de vídeo. Para obtener una lista de los comandos de MCI reconocidos por los dispositivos de vídeo digital, vea [Digital-Video Command Set](digital-video-command-set.md).

El controlador MCIAVI reproduce secuencias de vídeo y otros flujos de datos bajo el control de los comandos de MCI. Los flujos de datos pueden contener imágenes, audio y paletas. Los datos de imagen pueden constar de imágenes con paletas de colores o información de color verdadero.

El audio se sincroniza con el vídeo en una trigésima parte de un segundo. Sin embargo, si el hardware de audio no está disponible, el controlador reproduce solo la secuencia de vídeo. El controlador MCIAVI puede quitar fotogramas de vídeo, si es necesario, para reproducir una secuencia sin interrupción del audio.

La aplicación puede usar los servicios de clase de ventana MCIWnd en lugar de la interfaz de comandos de MCI para controlar cualquier controlador MCI. Esta clase de ventana controla muchos de los detalles de la administración de la ventana que admite el dispositivo MCI y simplifica la programación necesaria para enviar los comandos de MCI. La aplicación puede usar los servicios de biblioteca MCIWnd directamente para controlar el dispositivo MCI, o puede hacer que MCIWnd muestre una barra de herramientas, una barra de desplazamiento y menús que permiten al usuario controlar el dispositivo. Para obtener más información sobre la clase de ventana MCIWnd, vea [Clase de ventana MCIWnd](mciwnd-window-class.md).

 

 




