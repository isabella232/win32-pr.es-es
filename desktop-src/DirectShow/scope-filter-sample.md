---
description: Ejemplo de filtro de ámbito
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Ejemplo de filtro de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a931238b21dd604e7ca5de7943fcb2e85446f002a04ea0826dee9322dc6c7100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951964"
---
# <a name="scope-filter-sample"></a>Ejemplo de filtro de ámbito

## <a name="description"></a>Descripción

El filtro Ámbito es un filtro de representador que muestra datos de sonido como formas de onda.

## <a name="usage"></a>Uso

Para usar este filtro, abra GraphEdit y represente un archivo de audio (o un archivo de vídeo con una secuencia de audio). Desconecte temporalmente el representador de audio e inserte el filtro Infinite-Pin ejemplo de tee (ejemplo de filtro[inftee).](inftee-filter-sample.md) Vuelva a conectar el representador de audio. A continuación, Infinite-Pin el segundo pin de salida del filtro Tee al filtro Ámbito. Ahora ejecute el gráfico.

La ventana Ámbito se implementa como un cuadro de diálogo, no como una ventana real. Es posible que los desarrolladores que crean paneles de control para modificar los parámetros de filtro en tiempo real quieran usar una técnica como esta en lugar de páginas de propiedades.

El filtro Ámbito muestra cómo configurar un subproceso independiente para procesar los datos. En este caso, los datos simplemente se copian en un búfer independiente en el método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) y, a continuación, se dibujan en la ventana Ámbito del subproceso independiente.

El filtro Ámbito también le permite supervisar la salida de audio para determinar si está recortando, de modo que pueda ajustar la ganancia.

Este filtro aparece en GraphEdit como "Oscilscope".

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: *\[ Sdk Root \]* Samples Multimedia DirectShow Filters Scope (Ámbito de filtros \\ multimedia de ejemplos raíz del \\ \\ \\ \\ SDK).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



