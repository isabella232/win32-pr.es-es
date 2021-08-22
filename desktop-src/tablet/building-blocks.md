---
description: Hay varios formatos de persistencia que genera la plataforma tablet PC que son útiles como bloques de creación para los formatos enumerados anteriormente. Todos los formatos siguientes se generan y consumen mediante los métodos Load y Save del objeto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Bloques de creación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dbf34cc0159bdf2efe9b68255292a8b644ab10e684f44c11fa60d484bd45516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714295"
---
# <a name="building-blocks"></a>Bloques de creación

Hay varios formatos de persistencia que genera la plataforma tablet PC que son útiles como bloques de creación para los formatos enumerados anteriormente. Todos los formatos siguientes se [](/previous-versions/ms583670(v=vs.100)) generan y consumen mediante los métodos Load y [**Save del objeto**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) [**Ink.**](/previous-versions/ms569609(v=vs.100))

-   Formato serializado de entrada de lápiz (ISF): Ink Serialized Format (ISF) es la representación persistente más compacta de la entrada de lápiz. Puede insertar ISF en un formato de documento binario o moverlo directamente al Portapapeles. La entrada de lápiz almacenada en ISF debe usar el sistema de coordenadas predeterminado, que es HIMETRIC, con el eje vertical invertido.
-   ISF codificado en base 64: puede usar ISF codificado en base 64 para codificar la entrada de lápiz directamente en un archivo lenguaje de marcado extensible (XML) o HTML.
-   Archivo Formato de intercambio de gráficos (GIF) notificado: GIF notificado es un archivo GIF que contiene ISF como metadatos insertados en el archivo. La entrada de lápiz generada como GIF con notificación se puede ver en aplicaciones que no reconocen la entrada de lápiz, y todos los datos de entrada de lápiz se mantienen si la entrada de lápiz vuelve a una aplicación que sí reconoce la entrada de lápiz. Este formato es ideal para transportar contenido de entrada manuscrita dentro de un archivo HTML. La entrada de lápiz está disponible para cualquier aplicación, independientemente de si la aplicación reconoce la entrada de lápiz.
-   GIF con codificación base 64 fortified: este formato se proporciona para los desarrolladores que desean codificar la entrada manuscrita directamente en un archivo XML o HTML y, a continuación, convertir el archivo en una imagen más adelante. Puede usarlo cuando desee que un archivo XML generado contenga toda la información de entrada manuscrita y se use como una manera de generar HTML mediante transformaciones extensibles del lenguaje de hojas de estilos (XSLT).
    > [!Note]  
    > La tecnología de compresión y descompresión LZW está cubierta de forma inejepresa por el Us Patent No. 4.558.302 y sus correspondientes y otras subsidiarias (colectivamente, las LZW Patentas) propiedad de Unisys Corporation. Microsoft Corporation ha obtenido una licencia de Unisys en virtud de LZW Patentas para usar el GIF y la tecnología LZW en determinados productos de Microsoft. Sin embargo, esta licencia no se extiende a desarrolladores de terceros que usan productos de desarrollo de Microsoft, como el kit de herramientas de Microsoft y los productos de desarrollo de lenguaje, para proporcionar lectura y escritura GIF o cualquier otra funcionalidad de LZW en sus propios productos. Los desarrolladores de terceros deben tomar su propia determinación sobre si necesitan una licencia de Unisys para sus productos.

     

Una aplicación puede generar uno de estos formatos persistentes mediante el método [Microsoft.Ink.Stroke.HitTest](/previous-versions/ms828460(v=msdn.10)) o [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para generar una colección de trazos y:

-   Agregar estos trazos a un nuevo [**objeto Ink**](/previous-versions/ms583670(v=vs.100)) mediante el [método AddStrokesAtRectangle.](/previous-versions/ms569548(v=vs.100))
-   Generar un nuevo objeto [**Ink**](/previous-versions/ms583670(v=vs.100)) mediante el [método ExtractStrokes.](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))

El primero traduce el rectángulo de selección al origen, mientras que el segundo no. A continuación, la aplicación [**usa el método Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [**Ink.**](/previous-versions/ms583670(v=vs.100))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos sInk y tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
