---
description: El lector de origen es una alternativa al uso de la sesión multimedia y la canalización Microsoft Media Foundation para procesar los datos multimedia.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lector de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543798"
---
# <a name="source-reader"></a>Lector de origen

El lector de origen es una alternativa al uso de la [sesión multimedia](media-session.md) y la canalización Microsoft Media Foundation para procesar los datos multimedia.

## <a name="why-use-the-source-reader"></a>¿Por qué usar el lector de origen?

Media Foundation proporciona una canalización optimizada para la reproducción. La canalización es de un extremo a otro, lo que significa que controla el flujo de datos desde el origen (como un archivo de vídeo) hasta el destino (por ejemplo, la presentación de gráficos). Sin embargo, si desea leer o modificar los datos a medida que van a través de la canalización, debe escribir un complemento personalizado. Esto requiere un conocimiento bastante profundo de la canalización de Media Foundation. Para determinadas tareas, la creación de un nuevo complemento es demasiada sobrecarga. El lector de origen está diseñado para este tipo de situación, cuando desea obtener los datos sin procesar de un origen sin la sobrecarga de toda la canalización.

Internamente, el lector de origen contiene un puntero a un origen de medios. Un *origen multimedia* es un objeto Media Foundation que genera datos multimedia a partir de un origen externo, como un archivo multimedia o un dispositivo de captura de vídeo. El lector de origen administra todas las llamadas al método en el origen del medio. (Para obtener más información acerca de los orígenes multimedia, consulte [orígenes multimedia](media-sources.md)).

Si el origen multimedia entrega datos comprimidos, puede utilizar el lector de origen para descodificar los datos. En ese caso, el lector de código fuente cargará el descodificador correcto y administrará el flujo de datos entre el origen del medio y el descodificador. El lector de origen también puede realizar un procesamiento de vídeo limitado: conversión de color de YUV a RGB-32 y desentrelazado de software, aunque estas operaciones no se recomiendan para la representación de vídeo en tiempo real. En la imagen siguiente se ilustra este proceso.

![diagrama del lector de origen](images/sourcereader.png)

El lector de origen no envía los datos a un destino. depende de la aplicación usar los datos. Por ejemplo, el lector de origen puede leer un archivo de vídeo, pero no representará el vídeo en la pantalla. Además, el lector de origen no administra un reloj de presentación, controla los problemas de temporización ni sincroniza el vídeo con audio.

Considere la posibilidad de usar el lector de origen cuando:

-   Quiere obtener datos de un archivo multimedia sin preocuparse por la estructura de archivos subyacente.
-   Quiere obtener datos de un dispositivo de captura de audio o vídeo.
-   Las tareas de procesamiento de datos no distinguen el tiempo o no se requiere un reloj de presentación.
-   Ya dispone de una canalización multimedia que no se basa en Media Foundation y desea incorporar los orígenes de Media Foundation multimedia a su propia canalización.

No se recomienda el lector de origen en las siguientes situaciones:

-   Para contenido protegido. El lector de origen no admite la administración de derechos digitales (DRM).
-   Si le interesan los detalles de la estructura de archivos subyacente. El lector de origen oculta ese tipo de detalle.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                        | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Usar el lector de origen para procesar los datos multimedia](processing-media-data-with-the-source-reader.md)<br/> | En este tema se describe cómo usar el lector de origen para procesar datos multimedia.<br/>                                               |
| [Usar el lector de origen en modo asincrónico](using-the-source-reader-in-asynchronous-mode.md)<br/>  | En este tema se describe cómo usar el lector de origen en modo asincrónico.<br/>                                                |
| [Tutorial: descodificar audio](tutorial--decoding-audio.md)<br/>                                          | En este tutorial se muestra cómo usar el lector de origen para descodificar el audio de un archivo multimedia y escribir el audio en un archivo de sonido.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




