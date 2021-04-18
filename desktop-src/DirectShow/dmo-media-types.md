---
description: Tipos de medios DMO
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: Tipos de medios DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547427"
---
# <a name="dmo-media-types"></a>Tipos de medios DMO

Un tipo de medio describe el formato asociado a un flujo de datos multimedia. En este artículo se describe cómo administrar DMOs tipos de medios. Está destinado principalmente a desarrolladores que escriben sus propios DMOs personalizados.

Los tipos de medios se definen mediante la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Esta estructura incluye la siguiente información:

-   El *tipo principal* es un identificador único global (GUID) que define una amplia categoría, como audio o vídeo.
-   El *subtipo* es un GUID que define aspectos más específicos del tipo. Por ejemplo, en el vídeo, los subtipos incluyen el vídeo RGB de 16 bits, RGB de 24 bits, UYVY, codificado en DV, etc.
-   El *bloque de formato* es una estructura secundaria que especifica completamente el formato. El diseño del bloque de formato depende del tipo de datos. Por ejemplo, PCM audio usa la estructura **WAVEFORMATEX** . El vídeo usa otras estructuras, como **VIDEOINFOHEADER** y **VIDEOINFOHEADER2**. El diseño del bloque de formato se identifica mediante un GUID de tipo de formato. Por ejemplo, FORMAT \_ WaveFormatEx especifica una estructura **WaveFormatEx** .

Cuando se crea por primera vez una DMO, las secuencias no tienen un tipo de medio. Para que DMO pueda procesar los datos, el cliente debe establecer un tipo de medio para cada flujo. Este proceso se describe desde la perspectiva del cliente en el [establecimiento de tipos de medios en un DMO](setting-media-types-on-a-dmo.md).

**Tipos de medios en el registro**

Un DMO puede Agregar una lista de tipos de medios que admite al registro mediante una llamada a la función [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) . Una aplicación puede usar esta información para buscar DMOs que coincidan con un formato determinado. La información del registro no está pensada para ser exhaustiva. Normalmente, incluiría solo los tipos principales que admite DMO. La entrada del registro tiene claves independientes para los tipos de entrada y salida, pero no distingue entre flujos individuales.

La función **DMORegister** utiliza la estructura de [**\_ \_ MEDIATYPE parcial de DMO**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) para describir los tipos de medios. Esta estructura contiene un subconjunto de la información que se encuentra en la estructura de **\_ \_ tipo de medio DMO** , es decir, el tipo principal y el subtipo. No incluye un bloque de formato, porque el bloque de formato contiene normalmente información que es demasiado granular para incluirla en el registro, como el alto y el ancho de una imagen de vídeo.

**Tipos de medios preferidos**

Una vez que la aplicación ha creado un DMO, puede consultar a DMO los tipos de medios que admite. Para cada flujo, DMO crea una lista de tipos de medios (posiblemente vacíos), clasificada en orden de preferencia. Los métodos [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) y [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumeran los tipos preferidos. Los tipos preferidos de un flujo pueden cambiar dinámicamente cuando la aplicación establece tipos de medios en otras secuencias. Por ejemplo, la lista de tipos de salida preferidos podría cambiar después de establecer el tipo de entrada, o viceversa. Sin embargo, no es necesario que DMO actualice sus tipos preferidos dinámicamente. La aplicación no puede suponer que todos los tipos que recibe son válidos. Por esta razón, los métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) y [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) admiten una marca para probar un tipo específico.

Los métodos **GetInputType** y **GetOutputType** devuelven una estructura de **\_ \_ tipo de medio DMO** . DMO puede dejar en blanco parte de la información de esta estructura para indicar un intervalo de tipos. El tipo o subtipo principal puede ser el GUID \_ null y el bloque de formato puede estar vacío (cero bytes). Si el bloque de formato está vacío, el tipo de formato debe ser GUID \_ null.

Una vez que la aplicación establece todos los tipos de entrada de DMO, el DMO debe devolver generalmente al menos un tipo completo para cada flujo de salida. Un tipo de resultado completo facilita las pruebas y las aplicaciones pueden utilizarlo como valor predeterminado razonable. La aplicación de prueba de DMO se basa en este comportamiento. (Consulte [uso de la aplicación DMOTest](using-the-dmotest-application.md)).

**Establecer los tipos de medios**

Las aplicaciones usan los métodos **SetInputType** y **SetOutputType** para probar, establecer o borrar tipos en una secuencia especificada. La aplicación debe especificar por completo el tipo. DMO comprueba si puede aceptar el tipo propuesto. La respuesta puede depender de qué tipos se han establecido en otras secuencias. La \_ marca DMO set \_ TYPEF \_ Clear borra el tipo de una secuencia, por lo que la aplicación puede "deshacer" y probar otra combinación.

**Escenarios de ejemplo**

En los siguientes ejemplos se describen algunos escenarios típicos para ilustrar los puntos realizados en las secciones anteriores.

-   **Descodificadores de vídeo.** En un descodificador de vídeo típico, el tipo de entrada determina en parte el tipo de salida. Por ejemplo, normalmente ambas secuencias deben tener la misma velocidad de fotogramas y dimensiones de imagen. Una opción no es definir ningún tipo de salida preferido hasta que se establezca el tipo de entrada. Otra opción es enumerar un conjunto de tipos incompletos, omitiendo el bloque de formato. Use el subtipo para indicar los tipos sin comprimir admitidos, como RGB de 16 bits, RGB de 24 bits, etc. Además, los descodificadores de vídeo no admiten normalmente el establecimiento del tipo de salida antes del tipo de entrada. El escenario habitual es descodificar a partir de un formato de entrada conocido, por lo que esta limitación es razonable.
-   **Descodificadores de audio.** Un descodificador de audio podría admitir un conjunto limitado y fijo de formatos de salida. En ese caso, es posible que pueda crear una lista de formatos de salida preferidos antes de que se conozca el formato de entrada.
-   **Compresores.** En la mayoría de los casos, un compresor de vídeo no puede especificar por completo sus formatos de salida preferidos hasta que la aplicación establece el formato de entrada y viceversa. En su lugar, DMO debe devolver un tipo incompleto sin bloque de formato. En el caso de la compresión de audio y vídeo, la aplicación normalmente necesita establecer varios parámetros de salida, como la velocidad de bits. Sin embargo, después de establecer el tipo de entrada, el compresor debe devolver al menos un tipo de salida completo, por las razones mencionadas anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de DMO](writing-a-dmo.md)
</dt> </dl>

 

 



