---
description: Acerca de los filtros de DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Acerca de los filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554865"
---
# <a name="about-directshow-filters"></a>Acerca de los filtros de DirectShow

DirectShow usa una arquitectura modular, donde cada fase de procesamiento se realiza mediante un objeto COM denominado filtro. DirectShow proporciona un conjunto de filtros estándar para que los usen las aplicaciones, y los desarrolladores pueden escribir sus propios filtros personalizados que amplían la funcionalidad de DirectShow. Para ilustrar, estos son los pasos necesarios para reproducir un archivo de vídeo AVI, junto con los filtros que realizan cada paso:

-   Lea los datos sin procesar del archivo como una secuencia de bytes (filtro de origen de archivo).
-   Examine los encabezados AVI y analice el flujo de bytes en fotogramas de vídeo y muestras de audio independientes (filtro de divisor de AVI).
-   Descodifique los fotogramas de vídeo (varios filtros del descodificador, dependiendo del formato de compresión).
-   Dibuje los fotogramas de vídeo (filtro de representador de vídeo).
-   Enviar los ejemplos de audio a la tarjeta de sonido (filtro de dispositivo DirectSound predeterminado).

Estos filtros se muestran en el diagrama siguiente.

![gráfico de filtro para reproducir un archivo AVI con vídeo comprimido](images/avi-filter-graph.png)

Como se muestra en el diagrama, cada filtro está conectado a uno o varios filtros. Los puntos de conexión también son objetos COM, denominados *PIN*. Los filtros utilizan PIN para trasladar los datos de un filtro a la siguiente. Las flechas del diagrama muestran la dirección en la que los datos viajan. En DirectShow, un conjunto de filtros se denomina *gráfico de filtro*.

Los filtros tienen tres Estados posibles: en ejecución, detenido y en pausa. Cuando se ejecuta un filtro, procesa los datos multimedia. Cuando se detiene, detiene el procesamiento de los datos. El estado pausado se usa para señalar los datos antes de ejecutarse; en el [flujo de datos de](data-flow-in-the-filter-graph.md) la sección del gráfico de filtros se describe con más detalle este concepto. Con excepciones muy poco frecuentes, los cambios de estado se coordinan en todo el gráfico de filtros. todos los filtros del gráfico cambian de estado en el unísono. Por lo tanto, también se dice que todo el gráfico de filtros está en ejecución, detenido o en pausa.

Los filtros se pueden agrupar en varias categorías amplias:

-   Un filtro de *origen* introduce los datos en el gráfico. Los datos pueden provienen de un archivo, una red, una cámara o cualquier otro lugar. Cada filtro de origen controla un tipo diferente de origen de datos.
-   Un filtro de *transformación* toma un flujo de entrada, procesa los datos y crea un flujo de salida. Los codificadores y descodificadores son ejemplos de filtros de transformación.
-   Los filtros de *representador* se encuentran al final de la cadena. Reciben datos y los presentan al usuario. Por ejemplo, un representador de vídeo dibuja fotogramas de vídeo en la pantalla. un representador de audio envía datos de audio a la tarjeta de sonido. y un filtro de escritura de archivos escribe datos en un archivo.
-   Un filtro *divisor* divide un flujo de entrada en dos o más salidas, normalmente analizando el flujo de entrada a lo largo del proceso. Por ejemplo, el divisor AVI analiza una secuencia de bytes en secuencias de audio y vídeo independientes.
-   Un filtro *MUX* toma varias entradas y las combina en una única secuencia. Por ejemplo, AVI MUX realiza la operación inversa del divisor de AVI. Toma secuencias de audio y vídeo y genera una secuencia de bytes con formato AVI.

Las distinciones entre estas categorías no son absolutas. Por ejemplo, el filtro lector ASF actúa como filtro de origen y como filtro divisor.

Todos los filtros de DirectShow exponen la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) y todos los pin exponen la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . DirectShow también define muchas otras interfaces que admiten una funcionalidad más específica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de gráficos de filtros](about-the-filter-graph-manager.md)
</dt> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



