---
title: Capturar directamente desde un dispositivo a un archivo ASF (QASF)
description: Capturar directamente desde un dispositivo a un archivo ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows SDK de formato multimedia, captura desde dispositivos a archivos ASF (QASF)
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF), captura desde dispositivos (QASF)
- ASF (formato de sistemas avanzados), captura desde dispositivos (QASF)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, capturar desde dispositivos a archivos ASF (QASF)
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e773e39b4c2d76bd95f0a4ac90269be295585ef91e6e50f653b121cbc8d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705099"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Capturar directamente desde un dispositivo a un archivo ASF (QASF)

Al capturar audio o vídeo directamente en un archivo ASF, el gráfico de filtro tiene un aspecto similar al del diagrama siguiente, en función del tipo de dispositivo de captura que se esté utilizando.

![gráfico de captura de cámara web a wmv](images/asf-webcam.png)

La documentación del SDK de DirectShow describe en detalle cómo crear gráficos de captura, pero hay un punto importante que recordar al crear gráficos de captura mediante WM ASF Writer: WM ASF Writer no se ejecutará a menos que todos sus pines estén conectados. Si configura WM ASF Writer con el perfil de sistema predeterminado (no recomendado) o cualquier perfil con secuencias de audio y vídeo, se creará un pin de entrada para cada secuencia y cada uno de esos pines debe estar conectado. Si no piensa capturar audio, por ejemplo, asegúrese de configurar el filtro con un perfil de solo vídeo para que no se cree ninguna marca de audio.

 

 




