---
title: Cuadros de diálogo de vídeo
description: Cuadros de diálogo de vídeo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE mensaje
- CapDlgVideoSource macro
- WM_CAP_DLG_VIDEOFORMAT mensaje
- CapDlgVideoFormat macro
- WM_CAP_DLG_VIDEODISPLAY mensaje
- CapDlgVideoDisplay macro
- WM_CAP_DLG_VIDEOCOMPRESSION mensaje
- capDlgVideoCompression macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071724"
---
# <a name="video-dialog-boxes"></a>Cuadros de diálogo de vídeo

Cada controlador de captura puede proporcionar hasta cuatro cuadros de diálogo para controlar aspectos del proceso de digitalización y captura de vídeo, y para definir los atributos de compresión utilizados para reducir el tamaño de los datos de vídeo. El contenido de estos cuadros de diálogo se define mediante el controlador de captura de vídeo.

El cuadro de diálogo Origen de vídeo controla la selección de los canales de entrada de vídeo y los parámetros que afectan a la imagen de vídeo que se digitaliza en el búfer de fotogramas. Este cuadro de diálogo enumera los tipos de señales que conectan el origen de vídeo a la tarjeta de captura (normalmente SVHS y entradas compuestas) y proporciona controles para cambiar el matiz, el contraste o la saturación. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje [**\_ \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md) DE WM CAP (o la macro [**capDlgVideoSource).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource)

El cuadro de diálogo Formato de vídeo controla la selección de las dimensiones de fotogramas de vídeo digitalizados, la profundidad de la imagen y las opciones de compresión del vídeo capturado. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje [**\_ \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) de WM CAP (o la macro [**capDlgVideoFormat).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat)

El cuadro de diálogo Presentación de vídeo controla la apariencia del vídeo en el monitor durante la captura. Los controles de este cuadro de diálogo no tienen ningún efecto en los datos de vídeo digitalizados, pero podrían afectar a la presentación de la señal digitalizado. Por ejemplo, los dispositivos de captura que admiten la superposición pueden permitir modificar el matiz y la saturación, el color de la clave o la alineación de la superposición. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje [**\_ \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) de WM CAP (o la macro [**capDlgVideoDisplay).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay)

El cuadro de diálogo Compresión de vídeo controla los atributos de compresión de vídeo posteriores a la captura. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje [**\_ \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) de WM CAP (o la macro [**capDlgVideoCompression).**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression)

 

 




