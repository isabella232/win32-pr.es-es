---
description: El Lector de origen es una alternativa al uso de la sesión multimedia y la canalización Microsoft Media Foundation para procesar datos multimedia.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lector de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574760"
---
# <a name="source-reader"></a>Lector de origen

El Lector de origen es una alternativa al uso de [la](media-session.md) sesión multimedia y la canalización Microsoft Media Foundation para procesar datos multimedia.

## <a name="why-use-the-source-reader"></a>¿Por qué usar el lector de origen?

Media Foundation proporciona una canalización optimizada para la reproducción. La canalización es de un extremo a otro, lo que significa que controla el flujo de datos desde el origen (por ejemplo, un archivo de vídeo) hasta el destino (por ejemplo, la pantalla de gráficos). Sin embargo, si desea leer o modificar los datos a medida que pasan por la canalización, debe escribir un complemento personalizado. Esto requiere un conocimiento bastante profundo de la canalización Media Foundation datos. Para ciertas tareas, crear un nuevo complemento es demasiada sobrecarga. El lector de origen está diseñado para este tipo de situación, cuando desea obtener los datos sin procesar de un origen sin la sobrecarga de toda la canalización.

Internamente, el lector de origen contiene un puntero a un origen multimedia. Un *origen multimedia* es un Media Foundation que genera datos multimedia a partir de un origen externo, como un archivo multimedia o un dispositivo de captura de vídeo. El lector de origen administra todas las llamadas de método al origen multimedia. (Para obtener más información sobre los orígenes de medios, vea [Orígenes de medios).](media-sources.md)

Si el origen multimedia entrega datos comprimidos, puede usar el lector de origen para descodificar los datos. En ese caso, el lector de origen cargará el descodificador correcto y administrará el flujo de datos entre el origen multimedia y el descodificador. El lector de origen también puede realizar un procesamiento de vídeo limitado: conversión de color de YUV a RGB-32 y desenlazado de software, aunque estas operaciones no se recomiendan para la representación de vídeo en tiempo real. En la imagen siguiente se muestra este proceso.

![diagrama del lector de origen](images/sourcereader.png)

El lector de origen no envía los datos a un destino; es la aplicación la que debe consumir los datos. Por ejemplo, el lector de origen puede leer un archivo de vídeo, pero no representará el vídeo en la pantalla. Además, el lector de origen no administra un reloj de presentación, controla los problemas de control de tiempo ni sincroniza vídeo con audio.

Considere la posibilidad de usar el lector de origen cuando:

-   Quiere obtener datos de un archivo multimedia sin preocuparse por la estructura de archivos subyacente.
-   Quiere obtener datos de un dispositivo de captura de audio o vídeo.
-   Las tareas de procesamiento de datos no distinguen el tiempo o no se requiere un reloj de presentación.
-   Ya tiene una canalización multimedia que no se basa en Media Foundation y desea incorporar los orígenes multimedia de Media Foundation a su propia canalización.

No se recomienda el lector de origen en las situaciones siguientes:

-   Para el contenido protegido. El lector de origen no admite la administración de derechos digitales (DRM).
-   Si le importan los detalles de la estructura de archivos subyacente. El lector de origen oculta ese tipo de detalle.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                        | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Uso del Lector de origen para procesar datos multimedia](processing-media-data-with-the-source-reader.md)<br/> | En este tema se describe cómo usar el Lector de origen para procesar datos multimedia.<br/>                                               |
| [Uso del lector de origen en modo asincrónico](using-the-source-reader-in-asynchronous-mode.md)<br/>  | En este tema se describe cómo usar el Lector de origen en modo asincrónico.<br/>                                                |
| [Tutorial: Decoding Audio](tutorial--decoding-audio.md)<br/>                                          | En este tutorial se muestra cómo usar el Lector de origen para descodificar audio de un archivo multimedia y escribir el audio en un archivo WAVE.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




