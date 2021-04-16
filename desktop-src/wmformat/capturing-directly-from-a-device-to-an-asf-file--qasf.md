---
title: Captura directa desde un dispositivo a un archivo ASF (QASF)
description: Captura directa desde un dispositivo a un archivo ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media Format SDK, captura de dispositivos en archivos ASF (QASF)
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), captura desde dispositivos (QASF)
- ASF (formato de sistemas avanzados), captura desde dispositivos (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, captura de dispositivos en archivos ASF (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714199"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Captura directa desde un dispositivo a un archivo ASF (QASF)

Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtros es similar al diagrama siguiente, en función del tipo de dispositivo de captura que se esté usando.

![gráfico de captura de cámara web para WMV](images/asf-webcam.png)

En la documentación del SDK de DirectShow se describe en detalle cómo crear gráficos de captura, pero hay un punto importante que debe recordar al crear gráficos de captura con el escritor ASF de WM: el escritor ASF de WM no se ejecutará a menos que todos los pin estén conectados. Si configura el escritor ASF de WM con el perfil de sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un PIN de entrada para cada flujo y cada uno de esos PIN debe estar conectado. Si no desea capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ningún PIN de audio.

 

 




