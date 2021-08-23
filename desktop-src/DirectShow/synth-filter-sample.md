---
description: Ejemplo de filtro de síntesis
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Ejemplo de filtro de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a3a366a6612aadf653b5af13099dbc8a4f08c2fb828bca6e64514cb1801e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291204"
---
# <a name="synth-filter-sample"></a>Ejemplo de filtro de síntesis

## <a name="description"></a>Description

El filtro Synth es un filtro de origen que genera formas de onda de audio.

Este filtro muestra la creación de gráficos dinámicos. Puede cambiar entre el formato de audio PCM sin comprimir y el formato ADPCM de MS (microsoft \_ adaptive delta pulse code estadón) sin comprimir.

Este filtro aparece en GraphEdit como "Filtro de síntesis de audio".

Para obtener más información sobre la creación de gráficos dinámicos, vea [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="usage"></a>Uso

El filtro Synth permite al usuario establecer la forma de onda, la frecuencia, el número de canales y otras propiedades a través de la página de propiedades. Para establecer el punto de conexión superior o inferior del intervalo de frecuencia de la incoación, mantenga presionada la tecla MAYÚS mientras ajusta el control deslizante de frecuencia. El filtro también admite una interfaz personalizada, ISynth2, para establecer estas propiedades.

Para demostrar la característica de creación de gráficos dinámicos, haga lo siguiente:

1.  Compile el filtro y regístrelo con la utilidad Regsvr32.
2.  Inicie GraphEdit.
3.  Inserte el filtro de síntesis de audio. Aparece en la categoría DirectShow filtros.
4.  Represente el pin de salida del filtro.
5.  Haga clic en **el botón** Reproducir.
6.  Abra la página de propiedades del filtro.
7.  En el área Formato de salida, seleccione PCM o Microsoft ADPCM.

## <a name="programming-notes"></a>Notas de programación

Este ejemplo contiene los siguientes archivos:

-   Dynsrc.h, Dynsrc.cpp: contiene dos clases base para filtros de origen que admiten la creación de gráficos dinámicos, CDynamicSource y CDynamicSourceStream.
-   ISynth.h: declara la interfaz ISynth2 personalizada para establecer las propiedades en el filtro.
-   Resource.h: contiene constantes de recursos.
-   Synth.def: exporta las funciones DLL necesarias para la biblioteca COM.
-   Synth.h, Synth.cpp: contiene la clase CAudioSynth, que genera los datos de audio, y la clase CFilterFilter, que implementa el filtro.
-   Synth.rc: contiene los recursos utilizados por el filtro.
-   Synthprp.h, Synthprp.cpp: implementa la página de propiedades del filtro.

La clase CDynamicSource se adapta de la clase base [**CSource.**](csource.md) Usa uno o varios pins de salida derivados de la clase CDynamicSourceStream. La clase CDynamicSourceStream se adapta de la clase [**CSourceStream,**](csourcestream.md) pero se deriva de la clase [**CDynamicOutputPin**](cdynamicoutputpin.md) en lugar de la [**clase CBaseOutputPin.**](cbaseoutputpin.md)

La clase CDynamicSource tiene los métodos siguientes que no se encuentran en [**CSource**](csource.md):

-   Stop: señala el evento stop [**(CDynamicOutputPin::m \_ hStopEvent)**](cdynamicoutputpin-m-hstopevent.md)y apaga el subproceso de trabajo para todos los pines no conectados. En un pin conectado, el método inactivo del pin apagará el subproceso de trabajo.
-   Pausar: restablece el evento de detenerse.
-   JoinFilterGraph: llama al [**método CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) en cada pin.

La clase CDynamicSourceStream tiene los métodos siguientes que no se encuentran en [**CSourceStream**](csourcestream.md):

-   DestroySourceThread: apaga el subproceso de trabajo.
-   FatalError: indica un error al administrador de gráficos de filtro.
-   OutputPinNeedsToBeReconnected: indica que se debe volver a conectar el pin de salida. Cuando se llama a este método, el subproceso de trabajo llama al método [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) para volver a conectar el pin.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente de [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK \] Root* \\ Samples Multimedia DirectShow Filters \\ \\ \\ \\ Synth(Filtros multimedia de ejemplo raíz del SDK).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



