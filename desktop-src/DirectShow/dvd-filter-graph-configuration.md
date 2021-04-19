---
description: Configuración del gráfico de filtros de DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuración del gráfico de filtros de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537954"
---
# <a name="dvd-filter-graph-configuration"></a>Configuración del gráfico de filtros de DVD

En esta sección se describen las distintas configuraciones de gráficos de filtros para la reproducción de DVD en DirectShow. Estos diagramas se proporcionan principalmente como referencia. El navegador de DVD crea el gráfico, por lo que en general no es necesario comprender los detalles de cómo se configura el gráfico. Para obtener más información, vea [crear el gráfico de filtros de DVD](building-the-dvd-filter-graph.md).

En la ilustración siguiente se muestra un gráfico de filtros de DVD con un descodificador de software.

![gráfico de filtros de DVD para Windows XP](images/dvd-graph-xp.png)

Cuando un descodificador de hardware está presente, normalmente se conecta directamente a la tarjeta de vídeo mediante un puerto de vídeo. Esto permite que los bits de vídeo descodificados se envíen directamente al búfer de fotogramas de la tarjeta gráfica sin pasar a la memoria del host. Para administrar esta conexión directa en versiones anteriores de Windows, DirectShow es compatible con las extensiones de puerto de vídeo (VPE) de DirectDraw a través de una interfaz en el [filtro de mezclador de superposición](overlay-mixer-filter.md).

> [!Note]  
> El mezclador de superposición está ahora en desuso.

 

En Windows XP y versiones posteriores, un descodificador de hardware puede conectarse al filtro del [Administrador de puertos de vídeo](video-port-manager.md) .

![DVD Graph para Windows XP con un descodificador de hardware](images/dvd-hwgraph-xp.png)

En todos estos gráficos, el explorador de DVD es el filtro de origen; realiza varias tareas:

-   Lee los datos de navegación y vídeo del disco.
-   Desmultiplexa los datos de vídeo, audio y subimagen en flujos independientes.
-   Bombea los flujos en el gráfico para su posterior procesamiento y representación final.
-   Informa a la aplicación de eventos relacionados con DVD.

En la secuencia de audio, el explorador de DVD se conecta de nivel inferior a un descodificador de audio, que se conecta al [filtro de representador de DirectSound](directsound-renderer-filter.md), el representador de audio predeterminado. En las secuencias de vídeo y de subimagen, los filtros de nivel inferior son el descodificador de vídeo de terceros y el representador de mezcla de vídeo (o el [mezclador de superposición](overlay-mixer-filter.md)y el [representador de vídeo](video-renderer-filter.md) en aplicaciones de nivel inferior). Si la aplicación va a controlar los datos de subtítulos (CC) de la línea 21, debe agregar el filtro de la línea de código 21 de DirectShow al gráfico. Esto implica una única llamada al método; el filtro se conectará automáticamente.

La aplicación se comunica con el navegador de DVD y lo controla a través de las interfaces personalizadas que expone el navegador de DVD: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2): los métodos "SET" (y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)). También debe comunicarse con el administrador de gráficos de filtro (a través de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) para detener, iniciar y, de lo contrario, controlar el gráfico. Es posible que también necesite controlar otros filtros individuales, como el filtro de mezclador de superposición para cambiar entre la presentación en ventanas y la pantalla completa. Para obtener más información, vea [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). La configuración exacta del gráfico variará en función del tipo de descodificador MPEG-2 que haya instalado, independientemente de que sea necesario controlar los datos de subtítulos (CC) de línea 21 y otros factores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



