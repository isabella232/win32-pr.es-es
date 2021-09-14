---
description: Acerca de DirectShow filtros
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Acerca de DirectShow filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162489"
---
# <a name="about-directshow-filters"></a>Acerca de DirectShow filtros

DirectShow utiliza una arquitectura modular, donde cada fase de procesamiento la realiza un objeto COM denominado filtro. DirectShow proporciona un conjunto de filtros estándar para que las aplicaciones las usen, y los desarrolladores pueden escribir sus propios filtros personalizados que amplían la funcionalidad de DirectShow. Para ilustrar esto, estos son los pasos necesarios para reproducir un archivo de vídeo AVI, junto con los filtros que realizan cada paso:

-   Lea los datos sin procesar del archivo como una secuencia de bytes (filtro origen de archivo).
-   Examine los encabezados AVI y analice la secuencia de bytes en fotogramas de vídeo independientes y ejemplos de audio (filtro divisor AVI).
-   Descodificar los fotogramas de vídeo (varios filtros de descodificador, dependiendo del formato de compresión).
-   Dibuje los fotogramas de vídeo (filtro representador de vídeo).
-   Envíe los ejemplos de audio a la tarjeta de sonido (filtro predeterminado de dispositivo Direct Sound).

Estos filtros se muestran en el diagrama siguiente.

![gráfico de filtro para reproducir un archivo avi con vídeo comprimido](images/avi-filter-graph.png)

Como se muestra en el diagrama, cada filtro está conectado a uno o más filtros. Los puntos de conexión también son objetos COM, *denominados pins*. Los filtros usan pines para mover datos de un filtro al siguiente. Las flechas del diagrama muestran la dirección en la que viajan los datos. En DirectShow, un conjunto de filtros se denomina gráfico *de filtro*.

Los filtros tienen tres estados posibles: en ejecución, detenido y en pausa. Cuando se ejecuta un filtro, procesa los datos multimedia. Cuando se detiene, deja de procesar los datos. El estado en pausa se usa para proporcionar datos antes de ejecutarse; En la [sección Data Flow del filtro Graph](data-flow-in-the-filter-graph.md) describe este concepto con más detalle. Con excepciones muy poco frecuentes, los cambios de estado se coordinan en todo el gráfico de filtros; todos los filtros del gráfico cambian de estado al unísono. Por lo tanto, también se dice que todo el gráfico de filtros está en ejecución, detenido o en pausa.

Los filtros se pueden agrupar en varias categorías generales:

-   Un *filtro de* origen introduce datos en el gráfico. Los datos pueden proceder de un archivo, una red, una cámara o cualquier otro lugar. Cada filtro de origen controla un tipo diferente de origen de datos.
-   Un *filtro de* transformación toma un flujo de entrada, procesa los datos y crea un flujo de salida. Los codificadores y descodificadores son ejemplos de filtros de transformación.
-   *Los filtros del* representador se encuentra al final de la cadena. Reciben datos y los presentan al usuario. Por ejemplo, un representador de vídeo dibuja fotogramas de vídeo en la pantalla; un representador de audio envía datos de audio a la tarjeta de sonido; y un filtro de escritor de archivos escribe datos en un archivo.
-   Un *filtro divisor* divide un flujo de entrada en dos o más salidas, normalmente analizando el flujo de entrada a lo largo del proceso. Por ejemplo, el divisor AVI analiza una secuencia de bytes en secuencias de audio y vídeo independientes.
-   Un *filtro mux* toma varias entradas y las combina en una sola secuencia. Por ejemplo, el Mux avi realiza la operación inversa del divisor AVI. Toma secuencias de audio y vídeo y genera una secuencia de bytes con formato AVI.

Las diferencias entre estas categorías no son absolutas. Por ejemplo, el filtro lector de ASF actúa como filtro de origen y como filtro divisor.

Todos DirectShow filtros exponen la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) y todos los pines exponen la [**interfaz IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) DirectShow también define muchas otras interfaces que admiten funcionalidades más específicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de Graph filtros](about-the-filter-graph-manager.md)
</dt> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



