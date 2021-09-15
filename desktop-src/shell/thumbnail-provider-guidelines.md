---
description: Al proporcionar una miniatura, se deben seguir las instrucciones siguientes.
title: Directrices del controlador de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571460"
---
# <a name="thumbnail-handler-guidelines"></a>Directrices del controlador de miniaturas

Al proporcionar una miniatura, se deben seguir las instrucciones siguientes.

-   Proporcione miniaturas que se muestren bien con una resolución de 256 x 256 píxeles en color de 32 bits. El panel de lectura Windows Vista usa una miniatura de este tamaño en ausencia de un controlador de vista previa registrado. Sin embargo, un controlador de vista previa es la opción preferida y se debe proporcionar siempre que sea posible.
-   Cuando cree varias imágenes de diferentes tamaños, no cree las imágenes más pequeñas a partir de las más grandes recortando la página, el marco o la imagen. Reducir verticalmente toda la imagen.
-   No muestre varias páginas, marcos o imágenes a la vez; simplemente use uno. Si un documento consta de varias páginas, como un documento de texto o una hoja de cálculo que consta de varias hojas de cálculo, la página de portada suele ser la mejor opción, pero independientemente de cuál use, use solo una. No agregue páginas diferentes, lo que proporciona un aspecto desordenado.
-   Windows Vista es responsable de reducir o reducir verticalmente las imágenes de muestreo. Si al controlador se le pide una imagen más grande de la que tiene disponible, proporcione el tamaño más cercano que tenga. No intente cambiar dinámicamente el tamaño de su propia imagen.
-   Devuelve siempre una imagen en miniatura del controlador en lugar de realizar una lógica especial para devolver iconos tradicionales. Por debajo de un tamaño determinado, Windows Vista muestra automáticamente un icono tradicional en lugar de la miniatura. Consulte la sección *Caché de miniaturas y tamaño* de Controladores de [miniaturas](thumbnail-providers.md) para obtener más detalles.
-   Devuelva siempre una miniatura con la relación de aspecto de la página, el marco o la imagen. No use alfa para completar un cuadrado. Windows Vista es responsable de colocar correctamente una imagen no cuadrada.
-   No agregue adornos a las miniaturas. Windows Vista aplica automáticamente sombras paralelas y otros adornos cuando corresponda. También aplica adornos especiales para tipos de archivo específicos, como imágenes o vídeos.
-   No superponga el tipo de archivo ni la información de la aplicación en la miniatura. Windows Vista muestra automáticamente una superposición de tipos en la esquina inferior derecha de la imagen. Esta superposición se basa en el tipo percibido, pero se puede establecer para tipos de archivo individuales.
-   Para mejorar el rendimiento, cuando la miniatura se basa en el contenido del archivo (una página de un documento, por ejemplo) almacena la imagen de vista previa cuando el archivo se guarda (y, por tanto, probablemente cambia) en lugar de calcularlo en tiempo real. Esto debe hacerse si el cálculo consume mucha memoria (más de uno o dos segundos). Si no se hace esto, las vistas que muestran un gran número de archivos cuyas miniaturas se controlan mediante diferentes controladores van a tardar algún tiempo en mostrarse, una mala experiencia del usuario. Windows Vista almacena en caché las miniaturas y hace referencia a la hora de la última modificación para determinar si se debe actualizar una miniatura.
-   Tenga en cuenta que el Explorador puede optar por no mostrar una miniatura aunque haya un proveedor disponible. Por ejemplo, un archivo que se ha archivado en cinta no se recuperará para obtener su miniatura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de miniaturas](thumbnail-providers.md)
</dt> <dt>

[Compilar controladores de miniaturas](building-thumbnail-providers.md)
</dt> </dl>

 

 



