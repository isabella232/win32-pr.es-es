---
description: DMO Tipos de medios
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO Tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375247"
---
# <a name="dmo-media-types"></a>DMO Tipos de medios

Un tipo de medio describe el formato asociado a un flujo de datos multimedia. En este artículo se describe cómo las DDO controlan los tipos de medios. Está destinado principalmente a desarrolladores que escriben sus propias DDO personalizadas.

Los tipos de medios se definen mediante el [**DMO \_ estructura MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Esta estructura incluye la siguiente información:

-   El *tipo principal* es un identificador único global (GUID) que define una categoría amplia, como audio o vídeo.
-   El *subtipo* es un GUID que define aspectos más específicos del tipo. Por ejemplo, dentro del vídeo, los subtipos incluyen RGB de 16 bits, RGB de 24 bits, UYVY, vídeo codificado en DV, etc.
-   El *bloque de formato* es una estructura secundaria que especifica completamente el formato. El diseño del bloque de formato depende del tipo de datos. Por ejemplo, el audio PCM usa la **estructura DESATEX.** El vídeo usa otras estructuras, como **VIDEOINFOHEADER** y **VIDEOINFOHEADER2.** El diseño del bloque de formato se identifica mediante un GUID de tipo de formato. Por ejemplo, FORMAT \_ WaveFormatEx especifica una **estructura WAVEATEX.**

Cuando se crea DMO por primera vez, las secuencias no tienen un tipo de medio. Para que DMO procesar datos, el cliente debe establecer un tipo de medio para cada secuencia. Este proceso se describe desde la perspectiva del cliente en [Establecer tipos de medios en un DMO](setting-media-types-on-a-dmo.md).

**Tipos de medios en el Registro**

Un DMO puede agregar una lista de tipos de medios que admite al Registro mediante una llamada a la [**función DMORegister.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) Una aplicación puede usar esta información para buscar DDO que coincidan con un formato determinado. La información del Registro no está pensada para ser completa. Normalmente, incluiría solo los tipos principales que admite DMO principal. La entrada del Registro tiene claves independientes para los tipos de entrada y salida, pero no distingue entre secuencias individuales.

La **función DMORegister** usa la estructura [**DMO PARTIAL \_ \_ MEDIATYPE**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) para describir los tipos de medios. Esta estructura contiene un subconjunto de la información que se encuentra en la estructura **\_ DMO MEDIA \_ TYPE,** es decir, el tipo principal y el subtipo. No incluye un bloque de formato, porque el bloque de formato normalmente contiene información demasiado granular para incluirla en el Registro, como el alto y el ancho de una imagen de vídeo.

**Tipos de medios preferidos**

Una vez que la aplicación ha DMO, puede consultar el DMO los tipos de medios que admite. Para cada secuencia, el DMO crea una lista de tipos de medios (posiblemente vacíos), clasificados según el orden de preferencia. Los [**métodos IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) [**e IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumeran los tipos preferidos. Los tipos preferidos de una secuencia pueden cambiar dinámicamente cuando la aplicación establece tipos de medios en otras secuencias. Por ejemplo, la lista de tipos de salida preferidos puede cambiar después de establecer el tipo de entrada, o viceversa. Sin embargo, el DMO no es necesario para actualizar dinámicamente sus tipos preferidos. La aplicación no puede suponer que todos los tipos que recibe son válidos. Por este motivo, los métodos [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) admiten una marca para probar un tipo específico.

Los **métodos GetInputType** y **GetOutputType** devuelven un DMO **estructura MEDIA \_ \_ TYPE.** El DMO puede dejar parte de la información de esta estructura en blanco, para indicar un intervalo de tipos. El tipo principal o subtipo puede ser \_ GUID NULL y el bloque de formato puede estar vacío (cero bytes). Si el bloque de formato está vacío, el tipo de formato debe ser GUID \_ NULL.

Una vez que la aplicación establece todos los tipos de entrada de un DMO, el DMO generalmente debe devolver al menos un tipo completo para cada flujo de salida. Un tipo de salida completo facilita las pruebas y las aplicaciones pueden usarlas como un valor predeterminado razonable. La DMO de prueba se basa en este comportamiento. (Consulte [Uso de la aplicación DMOTest).](using-the-dmotest-application.md)

**Establecimiento de los tipos de medios**

Las aplicaciones usan **los métodos SetInputType** y **SetOutputType** para probar, establecer o borrar tipos en una secuencia especificada. La aplicación debe especificar completamente el tipo. El DMO comprueba si puede aceptar el tipo propuesto. La respuesta puede depender de qué tipos se han establecido en otras secuencias. El DMO marca SET TYPEF CLEAR borra el tipo de una secuencia, por lo que la aplicación puede \_ \_ "volver atrás" e intentar otra \_ combinación.

**Escenarios de ejemplo**

En los ejemplos siguientes se describen algunos escenarios típicos para ilustrar los puntos realizados en las secciones anteriores.

-   **Descodificadores de vídeo.** En un descodificador de vídeo típico, el tipo de entrada determina parcialmente el tipo de salida. Por ejemplo, normalmente ambas secuencias deben tener la misma velocidad de fotogramas y dimensiones de imagen. Una opción es no definir ningún tipo de salida preferido hasta que se establezca el tipo de entrada. Otra opción es enumerar un conjunto de tipos incompletos, omitiendo el bloque de formato. Use el subtipo para indicar los tipos no comprimidos admitidos, como RGB de 16 bits, RGB de 24 bits, etc. Además, los descodificadores de vídeo generalmente no admiten la configuración del tipo de salida antes del tipo de entrada. El escenario habitual es descodificar a partir de un formato de entrada conocido, por lo que esta limitación es razonable.
-   **Descodificadores de audio.** Un descodificador de audio puede admitir un conjunto limitado y fijo de formatos de salida. En ese caso, puede crear una lista de formatos de salida preferidos antes de que se conozca el formato de entrada.
-   **Compresores.** En la mayoría de los casos, un vídeo no puede especificar completamente sus formatos de salida preferidos hasta que la aplicación establece el formato de entrada y viceversa. En su lugar, DMO debe devolver un tipo incompleto sin bloque de formato. Para la compresión de audio y vídeo, la aplicación normalmente debe establecer varios parámetros de salida, como la velocidad de bits. Sin embargo, una vez establecido el tipo de entrada, el resalte debe devolver al menos un tipo de salida completo, por los motivos mencionados anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



