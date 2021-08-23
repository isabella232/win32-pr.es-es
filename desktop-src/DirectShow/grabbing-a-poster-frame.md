---
description: Captura de un marco de póster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Captura de un marco de póster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6668526d83f17c4ceab260f3a31ed43d19ec1d142bd8f8fdae080161350ded8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536575"
---
# <a name="grabbing-a-poster-frame"></a>Captura de un marco de póster

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe cómo mostrar un marco de póster desde un archivo multimedia digital mediante el objeto [Media Detector (MediaDet)](media-detector--mediadet.md) proporcionado con [DirectShow Editing Services](directshow-editing-services.md).

El Detector de medios es un objeto auxiliar que puede obtener información de formato de un archivo de origen multimedia. También puede tomar una imagen de mapa de bits de una secuencia de vídeo en el archivo de origen. Suponiendo que el archivo es buscable, puede obtener la imagen desde cualquier punto del archivo. La imagen devuelta siempre está en formato RGB de 24 bits.

El detector de medios no es un filtro y la aplicación no necesita usar el Administrador de filtros Graph ni crear un gráfico de filtros. Internamente, el detector de medios crea un gráfico de filtro que contiene el [**filtro de captura de ejemplo**](sample-grabber-filter.md). Para obtener un mapa de bits, el detector de medios busca y pausa el gráfico de filtro y, a continuación, recupera el mapa de bits del filtro Sample Grabber . La aplicación se comunica con el detector de medios a través de la [**interfaz IMediaDet.**](imediadet.md) El detector de medios es un buen ejemplo de encapsular un gráfico de filtro dentro de un objeto auxiliar, con el fin de proteger las aplicaciones de los detalles relacionados con el grafo.

El detector de medios funciona en dos modos. Cuando se crea por primera vez, el detector de medios está en modo de "recopilación de información". Puede especificar el nombre de un archivo multimedia y obtener información sobre cada una de las secuencias del archivo, como el tipo de formato, la velocidad de fotogramas o la duración. Si el archivo contiene una secuencia de vídeo, puede cambiar el detector de multimedia al modo de "captura de mapa de bits" y recuperar mapas de bits del origen. Sin embargo, una vez hecho esto, no puede volver a cambiar el Detector de medios a su modo original. se adjunta permanentemente a esa secuencia de vídeo. Para trabajar con otra secuencia u otro archivo, debe crear una nueva instancia de Media Detector.

> [!Note]  
> Los ejemplos de código de este tutorial usan la **clase CComPtr** atl, que administra automáticamente los recuentos de referencias. Si prefiere usar punteros de interfaz sin procesar, recuerde liberar todas las interfaces cuando haya terminado con ella. Además, por brevedad, los ejemplos de código omiten gran parte de la comprobación de errores que debe realizar una aplicación. En el código de trabajo, compruebe siempre **los valores HRESULT.**

 

Este tutorial contiene los siguientes pasos:

-   [Paso 1: Crear el marco Windows Framework](step-1--create-the-windows-framework.md)
-   [Paso 2: Agregar un comando de menú para agarrar un marco de póster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Paso 3: Implementar la función Frame-Grabbing trabajo](step-3--implement-the-frame-grabbing-function.md)
-   [Paso 4: Dibujar el mapa de bits en el área de cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 



