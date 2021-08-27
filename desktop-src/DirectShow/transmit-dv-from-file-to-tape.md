---
description: Transmisión de DV de archivo a cinta
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmisión de DV de archivo a cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bcd7bf716466cda2fc23a03968da4a51c005070f885183390f944d14994ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086795"
---
# <a name="transmit-dv-from-file-to-tape"></a>Transmisión de DV de archivo a cinta

La transmisión desde un archivo DV AVI a una cinta VTR se complica en cierto modo por el hecho de que los archivos pueden escribir 1 o 2. Para transmitir un archivo DV a cinta, haga lo siguiente:

1.  Cree una instancia del filtro [del controlador MSDV.](msdv-driver.md) Para obtener más información, consulte [Selección de un dispositivo de captura.](selecting-a-capture-device.md)
2.  Asegúrese de que el dispositivo está en modo VTR. De lo contrario, no se puede transmitir a cinta. Consulte [Modo de dispositivo](device-mode.md).
3.  Inicialice el Generador Graph captura, tal como se describe en [Acerca de la](about-the-capture-graph-builder.md)captura Graph Builder .
4.  Compile el gráfico. La configuración del grafo depende del tipo de archivo DV:
    -   [Transmisión desde un archivo de tipo 1](transmit-from-type-1-file.md)
    -   [Transmisión desde un archivo de tipo 2](transmit-from-type-2-file.md)
5.  Ponga el dispositivo en modo de pausa de registro, tal como se describe en [Control de una cámara DV.](controlling-a-dv-camcorder.md)
6.  Pausar el gráfico de filtro. Mientras el gráfico de filtros está en pausa, envía una secuencia continua que repite el primer fotograma del vídeo.
7.  Para empezar a transmitir, coloque el dispositivo en modo de registro y, a continuación, ejecute el gráfico de filtros. El dispositivo tarda una cantidad determinada de tiempo hasta que el responsable de la grabación puede grabar, por lo que debe esperar unos dos segundos antes de ejecutar el gráfico. Esto podría dar lugar a algunos fotogramas duplicados al principio de la cinta, pero garantiza que no se pierda ningún dato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



