---
description: Al proporcionar una miniatura, deben seguirse las siguientes directrices.
title: Instrucciones de controlador de miniaturas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: 9763c9cb859df3530766b6e65f9dce4f7de87fd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/11/2020
ms.locfileid: "104149744"
---
# <a name="thumbnail-handler-guidelines"></a>Instrucciones de controlador de miniaturas

Al proporcionar una miniatura, deben seguirse las siguientes directrices.

-   Proporcione vistas en miniatura que se muestren bien en una resolución de 256x256 píxeles en color de 32 bits. El panel de lectura de Windows Vista utiliza una miniatura de este tamaño en ausencia de un controlador de vista previa registrado. Sin embargo, un controlador de vista previa es la opción preferida y debe proporcionarse siempre que sea posible.
-   Al crear varias imágenes de diferentes tamaños, no cree las imágenes más pequeñas desde el mayor recortando la página, el marco o la imagen. Reducir verticalmente toda la imagen.
-   No mostrar varias páginas, marcos o imágenes a la vez; solo tiene que usar uno. Si un documento se compone de varias páginas, como un documento de texto o una hoja de cálculo que se compone de varias hojas de cálculo, la portada suele ser la mejor opción, pero independientemente de la que use, utilice solo una. No agregue páginas diferentes, lo que supone una apariencia abarrotada.
-   Windows Vista es responsable de escalar o reducir verticalmente las imágenes de muestreo. Si se le pide al controlador una imagen mayor de la que tiene disponible, proporcione el tamaño más cercano que tenga. No intente cambiar el tamaño de su propia imagen dinámicamente.
-   Devuelva siempre una imagen en miniatura del controlador en lugar de realizar una lógica especial para devolver los iconos tradicionales. Bajo un determinado tamaño, Windows Vista muestra automáticamente un icono tradicional en lugar de la miniatura. Para más información, consulte la sección *caché en miniatura y tamaño* de los [controladores de miniaturas](thumbnail-providers.md) .
-   Devuelva siempre una miniatura con la relación de aspecto de la página, el marco o la imagen. No utilice alfa para completar un cuadrado. Windows Vista es responsable de posicionar correctamente una imagen no cuadrada.
-   No agregue elementos gráficos a las miniaturas. Windows Vista aplica automáticamente las sombras paralelas y otros elementos gráficos cuando corresponda. También se aplican elementos gráficos especiales para tipos de archivo específicos, como imágenes o vídeos.
-   No superponga el tipo de archivo ni la información de la aplicación en la miniatura. Windows Vista muestra una superposición de tipo en la esquina inferior derecha de la imagen. Esta superposición se basa en el tipo percibido, pero se puede establecer para los tipos de archivo individuales.
-   Para mejorar el rendimiento, cuando la miniatura se basa en el contenido de un archivo (por ejemplo, una página de un documento), almacene la imagen de vista previa cuando se guarde el archivo (y, por lo tanto, cambie probablemente) en lugar de calcularlo en tiempo real. Esto se debe hacer si el cálculo tiene un uso intensivo de memoria (más de uno o dos segundos). Si no se hace esto, las vistas que muestran un gran número de archivos cuyas miniaturas se controlan mediante controladores diferentes van a tardar algún tiempo en mostrarse, una experiencia de usuario incorrecta. Windows Vista almacena en caché miniaturas y hace referencia a la hora de la última modificación para determinar si se debe actualizar una miniatura.
-   Tenga en cuenta que el explorador puede optar por no mostrar una miniatura aunque esté disponible un proveedor. Por ejemplo, un archivo que se ha archivado en cinta no se volverá a llamar para obtener su miniatura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores en miniatura](thumbnail-providers.md)
</dt> <dt>

[Crear controladores de miniaturas](building-thumbnail-providers.md)
</dt> </dl>

 

 



