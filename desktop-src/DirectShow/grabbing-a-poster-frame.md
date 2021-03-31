---
description: Captación de un fotograma de póster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Captación de un fotograma de póster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495773"
---
# <a name="grabbing-a-poster-frame"></a>Captación de un fotograma de póster

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe cómo mostrar un fotograma de póster desde un archivo multimedia digital mediante el objeto de [detección de medios (MediaDet)](media-detector--mediadet.md) proporcionado con los [servicios de edición de DirectShow](directshow-editing-services.md).

El detector de medios es un objeto auxiliar que puede obtener información de formato de un archivo de origen multimedia. También puede obtener una imagen de mapa de bits de una secuencia de vídeo en el archivo de código fuente. Suponiendo que se pueda buscar en el archivo, puede obtener la imagen de cualquier punto del archivo. La imagen devuelta siempre tiene el formato RGB de 24 bits.

El detector de medios no es un filtro y la aplicación no necesita usar el administrador de gráficos de filtro ni crear un gráfico de filtro. Internamente, el detector de medios crea un gráfico de filtros que contiene el [**filtro de enganche de ejemplo**](sample-grabber-filter.md). Para obtener un mapa de bits, el detector de medios busca y pone en pausa el gráfico de filtro y, a continuación, recupera el mapa de bits del filtro de enganche de ejemplo. La aplicación se comunica con el detector de medios a través de la interfaz [**IMediaDet**](imediadet.md) . El detector de medios es un buen ejemplo de encapsulación de un gráfico de filtro dentro de un objeto auxiliar, con el fin de proteger las aplicaciones de los detalles relacionados con los gráficos.

El detector de medios funciona en dos modos. Cuando se crea por primera vez, el detector de medios está en modo de "recopilación de información". Puede especificar el nombre de un archivo multimedia y obtener información sobre cada una de las secuencias del archivo, como el tipo de formato, la velocidad de fotogramas o la duración. Si el archivo contiene una secuencia de vídeo, puede cambiar el detector de medios al modo "captura de mapa de bits" y recuperar los mapas de bits del origen. Sin embargo, una vez hecho esto, no puede volver a cambiar el detector de medios a su modo original; está conectado permanentemente a esa secuencia de vídeo. Para trabajar con otro flujo u otro archivo, debe crear una nueva instancia del detector de medios.

> [!Note]  
> En los ejemplos de código de este tutorial se usa la clase **CComPtr** de ATL, que administra automáticamente los recuentos de referencias. Si prefiere usar punteros de interfaz sin formato, recuerde liberar todas las interfaces cuando haya terminado. Además, para mayor brevedad, los ejemplos de código omiten gran parte de la comprobación de errores que debe realizar una aplicación. En código de trabajo, compruebe siempre los valores **HRESULT** .

 

Este tutorial contiene los siguientes pasos:

-   [Paso 1: crear Windows Framework](step-1--create-the-windows-framework.md)
-   [Paso 2: agregar un comando de menú para capturar un fotograma de póster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Paso 3: implementar la función Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)
-   [Paso 4: dibujo del mapa de bits en el área cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



