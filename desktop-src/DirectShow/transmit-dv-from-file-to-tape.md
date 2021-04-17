---
description: Transmisión de DV desde un archivo a una cinta
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmisión de DV desde un archivo a una cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668278"
---
# <a name="transmit-dv-from-file-to-tape"></a>Transmisión de DV desde un archivo a una cinta

La transmisión desde un archivo AVI DV a una cinta VTR es complicada en cierto modo por el hecho de que los archivos pueden escribir-1 o el tipo 2. Para transmitir un archivo DV a una cinta, haga lo siguiente:

1.  Cree una instancia del filtro del [controlador MSDV](msdv-driver.md) . Para obtener más información, consulte [seleccionar un dispositivo de captura](selecting-a-capture-device.md).
2.  Asegúrese de que el dispositivo está en modo VTR. De lo contrario, no puede transmitir a cinta. Vea [modo de dispositivo](device-mode.md).
3.  Inicialice el generador de gráficos de captura, tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).
4.  Cree el gráfico. La configuración del gráfico depende del tipo de archivo DV:
    -   [Transmisión del archivo de tipo 1](transmit-from-type-1-file.md)
    -   [Transmisión desde el archivo de tipo 2](transmit-from-type-2-file.md)
5.  Ponga el dispositivo en modo de pausa de grabación, como se describe en [controlar una videocámara DV](controlling-a-dv-camcorder.md).
6.  PAUSE el gráfico de filtro. Mientras el gráfico de filtro está en pausa, envía un flujo continuo que repite el primer fotograma del vídeo.
7.  Para iniciar la transmisión, ponga el dispositivo en modo de registro y, a continuación, ejecute el gráfico de filtro. Tarda en el dispositivo una cantidad de tiempo determinada hasta que el encabezado de grabación pueda grabarse, por lo que debe esperar unos dos segundos antes de ejecutar el gráfico. Esto podría dar lugar a algunos fotogramas duplicados al principio de la cinta, pero garantiza que no se pierdan datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



