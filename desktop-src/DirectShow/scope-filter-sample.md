---
description: Ejemplo de filtro de ámbito
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Ejemplo de filtro de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494891"
---
# <a name="scope-filter-sample"></a>Ejemplo de filtro de ámbito

## <a name="description"></a>Descripción

El filtro de ámbito es un filtro de representador que muestra los datos de sonido como formas de onda.

## <a name="usage"></a>Uso

Para usar este filtro, abra GraphEdit y represente un archivo de audio (o un archivo de vídeo con una secuencia de audio). Desconecte el representador de audio temporalmente e inserte el filtro de ejemplo Infinite-Pin Tee ([ejemplo de filtro InfTee](inftee-filter-sample.md)). Vuelva a conectar el representador de audio. A continuación, conecte el segundo PIN de salida del filtro Infinite-Pin Tee al filtro de ámbito. Ahora ejecute el gráfico.

La ventana ámbito se implementa como un cuadro de diálogo, no como una ventana real. Los desarrolladores que crean paneles de control para modificar los parámetros de filtro en tiempo real pueden querer usar una técnica como esta en lugar de las páginas de propiedades.

El filtro de ámbito muestra la configuración de un subproceso independiente para procesar los datos. En este caso, los datos se copian en un búfer independiente en el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) y, a continuación, se dibujan en la ventana de ámbito en el subproceso independiente.

El filtro de ámbito también le permite supervisar la salida de audio para determinar si está recortando, de modo que pueda ajustar la ganancia.

Este filtro aparece en GraphEdit como "Oscilloscope".

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* ámbito de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



