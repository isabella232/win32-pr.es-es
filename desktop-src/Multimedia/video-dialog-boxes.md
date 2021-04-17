---
title: Cuadros de diálogo de vídeo
description: Cuadros de diálogo de vídeo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Mensaje WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource (macro)
- Mensaje WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat (macro)
- Mensaje WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay (macro)
- Mensaje WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665611"
---
# <a name="video-dialog-boxes"></a>Cuadros de diálogo de vídeo

Cada controlador de captura puede proporcionar hasta cuatro cuadros de diálogo para controlar aspectos del proceso de captura y digitalización de vídeo, y para definir los atributos de compresión que se usan para reducir el tamaño de los datos de vídeo. El contenido de estos cuadros de diálogo se define mediante el controlador de captura de vídeo.

El cuadro de diálogo origen de vídeo controla la selección de canales de entrada de vídeo y los parámetros que afectan a la imagen de vídeo que se está digitalizando en el búfer de fotogramas. En este cuadro de diálogo se enumeran los tipos de señales que conectan el origen de vídeo con la tarjeta de captura (normalmente SVHS y las entradas compuestas) y se proporcionan controles para cambiar el matiz, el contraste o la saturación. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ videosource Dlg Cap de WM**](wm-cap-dlg-videosource.md) (o la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).

El cuadro de diálogo formato de vídeo controla la selección de las dimensiones del fotograma de vídeo digitalizado y la profundidad de imagen, así como las opciones de compresión del vídeo capturado. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ videoformat de Cap Cap Dlg**](wm-cap-dlg-videoformat.md) (o la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).

El cuadro de diálogo presentación en vídeo controla la apariencia del vídeo en el monitor durante la captura. Los controles de este cuadro de diálogo no tienen ningún efecto en los datos de vídeo digitalizados, pero podrían afectar a la presentación de la señal digitalizada. Por ejemplo, los dispositivos de captura que admiten la superposición pueden permitir la modificación del matiz y la saturación, el color de la clave o la alineación de la superposición. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de vídeo de [**\_ \_ \_ presentación de Cap de WM Cap**](wm-cap-dlg-videodisplay.md) (o la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).

El cuadro de diálogo compresión de vídeo controla los atributos de compresión de vídeo posteriores a la captura. Si el cuadro de diálogo es compatible con un controlador de captura de vídeo, puede mostrarlo y actualizarlo mediante el mensaje de [**\_ \_ \_ compresión**](wm-cap-dlg-videocompression.md) de vídeo del Cap de WM (o la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).

 

 




