---
description: Configuración del filtro de DVD Graph DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuración del filtro de DVD Graph DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653096"
---
# <a name="dvd-filter-graph-configuration"></a>Configuración del filtro de DVD Graph DVD

En esta sección se describen las distintas configuraciones de gráfico de filtros para la reproducción de DVD DirectShow. Estos diagramas se proporcionan principalmente como referencia. Dvd Navigator compila el gráfico, por lo que en general no es necesario comprender los detalles de cómo se configura el grafo. Para obtener más información, vea [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

En la ilustración siguiente se muestra un gráfico de filtro de DVD con un descodificador de software.

![Gráfico de filtro de dvd para Windows XP](images/dvd-graph-xp.png)

Cuando hay un descodificador de hardware, normalmente se conecta directamente a la tarjeta de vídeo mediante un puerto de vídeo. Esto permite que los bits de vídeo descodificados se envíen directamente al búfer de fotogramas de la tarjeta gráfica sin pasar a la memoria del host. Para administrar esta conexión directa en versiones anteriores de Windows, DirectShow admite extensiones de puerto de vídeo (VPE) de DirectDraw a través de una interfaz en el filtro de [Mixer superposición](overlay-mixer-filter.md).

> [!Note]  
> El elemento Overlay Mixer está en desuso.

 

En Windows XP y versiones posteriores, un descodificador de hardware puede conectarse al filtro [Administrador de puertos de](video-port-manager.md) vídeo.

![gráfico de dvd para Windows XP con un descodificador de hardware](images/dvd-hwgraph-xp.png)

En todos estos gráficos, el navegador de DVD es el filtro de origen; realiza varias tareas:

-   Lee los datos de navegación y vídeo del disco.
-   Demultiplexa los datos de vídeo, audio y subpicture en secuencias independientes.
-   Procesa las secuencias en el gráfico para su posterior procesamiento y representación final.
-   Informa a la aplicación de eventos relacionados con DVD.

En la secuencia de audio, el navegador de DVD se conecta de bajada a un descodificador de audio, que se conecta al filtro de representador [de DirectSound](directsound-renderer-filter.md), el representador de audio predeterminado. En las secuencias de vídeo y subimagen, los filtros de bajada son el descodificador de vídeo de terceros, el representador de mezcla de vídeo (o el objeto [Overlay Mixer](overlay-mixer-filter.md)y [el](video-renderer-filter.md) representador de vídeo en aplicaciones de nivel inferior). Si la aplicación controlará los datos con subtítulos de la línea 21, debe agregar el filtro DirectShow Line 21 Decoder 2 al gráfico. Esto implica una sola llamada de método; el filtro se conectará automáticamente.

La aplicación se comunica con el navegador de DVD y lo controla a través de las interfaces personalizadas que expone el navegador de DVD: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)(los métodos "set" e [**IDvdInfo2),**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)los métodos "get". También debe comunicarse con el administrador de gráficos de filtro (a través de [**IMediaControl)**](/windows/desktop/api/Control/nn-control-imediacontrol)para detener, iniciar y controlar el gráfico de otro modo. También es posible que tenga que controlar otros filtros individuales, como el filtro overlay Mixer para cambiar entre la pantalla de ventana y la pantalla completa. Para obtener más información, [**vea IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). La configuración exacta del gráfico variará en función del tipo de descodificador MPEG-2 que haya instalado, si necesita controlar los datos con subtítulos de la línea 21 y otros factores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



