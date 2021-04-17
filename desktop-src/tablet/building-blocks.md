---
description: Hay varios formatos de persistencia que la plataforma de Tablet PC genera y que son útiles como bloques de creación para los formatos enumerados anteriormente. Los siguientes formatos se generan y consumen mediante los métodos Load y Save del objeto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Bloques de creación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705396"
---
# <a name="building-blocks"></a>Bloques de creación

Hay varios formatos de persistencia que la plataforma de Tablet PC genera y que son útiles como bloques de creación para los formatos enumerados anteriormente. Los siguientes formatos se generan y consumen mediante los métodos [**Load**](/previous-versions/ms569609(v=vs.100)) y [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

-   Formato serializado de tinta (ISF): el formato serializado de tinta (ISF) es la representación persistente más compacta de la tinta. Puede incrustar ISF dentro de un formato de documento binario o moverlo directamente al portapapeles. La entrada de lápiz almacenada en ISF debe utilizar el sistema de coordenadas predeterminado, que es HIMETRIC, con el eje vertical invertido.
-   ISF codificado en base 64: puede usar el ISF codificado en base 64 para codificar la entrada manuscrita directamente en un archivo lenguaje de marcado extensible (XML) o HTML.
-   Formato de intercambio de gráficos enriquecido (GIF): GIF alcoholizado es un archivo GIF que contiene ISF como metadatos insertados en el archivo. La tinta generada como un GIF enriquecido se puede ver en las aplicaciones que no reconocen la tinta y se mantienen todos los datos de tinta si la tinta se vuelve a una aplicación que reconoce la tinta. Este formato es ideal para transportar contenido de tinta dentro de un archivo HTML. La tinta está disponible para cualquier aplicación, independientemente de si la aplicación reconoce la tinta.
-   GIF alcoholizado codificado en base 64: este formato se proporciona para los programadores que desean codificar la entrada manuscrita directamente en un archivo XML o HTML y, a continuación, convertir el archivo en una imagen en otro momento. Puede utilizarlo si desea que un archivo XML que contenga toda la información de entrada manuscrita y que se use como una manera de generar HTML mediante las transformaciones del lenguaje de hojas de estilo extensible (XSLT).
    > [!Note]  
    > La tecnología LZW de compresión y descompresión es presuntamente tratada por el número de patentes de EE. UU. 4.558.302 y sus patentes relacionadas y equivalentes externas (colectivamente, las patentes de LZW) propiedad de Unisys Corporation. Microsoft Corporation ha obtenido una licencia de Unisys bajo las patentes de LZW para usar el GIF y la tecnología LZW en determinados productos de Microsoft. Sin embargo, esta licencia no se extiende a los desarrolladores de terceros que utilizan productos de desarrollo de Microsoft, como los productos de Microsoft Toolkit y desarrollo de lenguaje, para proporcionar GIF de lectura/escritura o cualquier otra funcionalidad LZW en sus propios productos. Los desarrolladores de terceros necesitan tomar su propia determinación de si necesitan una licencia de Unisys para sus productos.

     

Una aplicación puede generar uno de estos formatos persistentes mediante el método [Microsoft. Ink. Stroke. HitTest](/previous-versions/ms828460(v=msdn.10)) o [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para generar una colección de trazos y:

-   Agregar estos trazos a un nuevo objeto de [**entrada de lápiz**](/previous-versions/ms583670(v=vs.100)) mediante el método [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100)) .
-   Generar un nuevo objeto de [**entrada de lápiz**](/previous-versions/ms583670(v=vs.100)) mediante el método [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) .

El primero traduce el rectángulo de selección al origen, mientras que el segundo no lo hace. A continuación, la aplicación utiliza el método [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos sInk y tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
