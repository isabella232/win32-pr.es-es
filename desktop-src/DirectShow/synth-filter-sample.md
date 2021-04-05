---
description: Ejemplo de filtro de sintetizador
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Ejemplo de filtro de sintetizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913137"
---
# <a name="synth-filter-sample"></a>Ejemplo de filtro de sintetizador

## <a name="description"></a>Descripción

El filtro de sintetizador es un filtro de origen que genera perfiles de onda de audio.

Este filtro muestra la creación de gráficos dinámicos. Puede cambiar entre audio PCM sin comprimir y \_ formato MS ADPCM (modulación de código de Delta de Microsoft adaptable) comprimido.

Este filtro aparece en GraphEdit como "filtro de sintetizador de audio".

Para obtener más información sobre la creación de gráficos dinámicos, vea [creación de gráficos dinámicos](dynamic-graph-building.md).

## <a name="usage"></a>Uso

El filtro de sintetizador permite al usuario establecer la forma de onda, la frecuencia, el número de canales y otras propiedades a través de la página de propiedades. Para establecer el extremo superior o inferior del intervalo de frecuencia de barrido, mantenga presionada la tecla Mayús mientras ajusta el control deslizante de frecuencia. El filtro también admite una interfaz personalizada, ISynth2, para establecer estas propiedades.

Para demostrar la característica de creación de gráficos dinámicos, haga lo siguiente:

1.  Cree el filtro y regístrelo con la utilidad regsvr32.
2.  Inicie GraphEdit.
3.  Inserte el filtro de sintetizador de audio. Aparece en la categoría filtros de DirectShow.
4.  Representar el PIN de salida del filtro.
5.  Haga clic en el botón **reproducir** .
6.  Abra la página de propiedades del filtro.
7.  En el área formato de salida, seleccione PCM o Microsoft ADPCM.

## <a name="programming-notes"></a>Notas de programación

Este ejemplo contiene los siguientes archivos:

-   Dynsrc. h, dynsrc. cpp: contiene dos clases base para filtros de origen que admiten la creación de gráficos dinámicos, CDynamicSource y CDynamicSourceStream.
-   ISynth. h: declara la interfaz ISynth2 personalizada para establecer las propiedades del filtro.
-   Resource. h: contiene constantes de recursos.
-   Sint. def: exporta las funciones DLL que necesita la biblioteca COM.
-   Sint. h, Sint. cpp: contiene la clase CAudioSynth, que genera los datos de audio y la clase CSynthFilter, que implementa el filtro.
-   Sintetizador. RC: contiene los recursos utilizados por el filtro.
-   Synthprp. h, Synthprp. cpp: implementa la página de propiedades del filtro.

La clase CDynamicSource se adapta de la clase base [**CSource**](csource.md) . Usa uno o varios PIN de salida derivados de la clase CDynamicSourceStream. La clase CDynamicSourceStream se adapta de la clase [**CSourceStream**](csourcestream.md) , pero se deriva de la clase [**CDynamicOutputPin**](cdynamicoutputpin.md) en lugar de la clase [**CBaseOutputPin**](cbaseoutputpin.md) .

La clase CDynamicSource tiene los siguientes métodos no encontrados en [**CSource**](csource.md):

-   STOP: señala el evento STOP ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) y cierra el subproceso de trabajo para todos los PIN no conectados. En un PIN conectado, el método inactivo del PIN cerrará el subproceso de trabajo.
-   Pausar: restablece el evento de detención.
-   JoinFilterGraph: llama al método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) en cada pin.

La clase CDynamicSourceStream tiene los siguientes métodos no encontrados en [**CSourceStream**](csourcestream.md):

-   DestroySourceThread: cierra el subproceso de trabajo.
-   FatalError: indica un error al administrador de gráficos de filtro.
-   OutputPinNeedsToBeReconnected: indica que el PIN de salida debe volver a conectarse. Cuando se llama a este método, el subproceso de trabajo llama al método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para volver a conectar el PIN.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz de SDK* de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



