---
description: El receptor de medios de ASF es el componente final de la canalización de codificación que permite a una aplicación escribir un archivo ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Receptores multimedia de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50af8530b1c2b8d9131243cafa67e841289cbbe0691cfcb499b57df68b60b141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744216"
---
# <a name="asf-media-sinks"></a>Receptores multimedia de ASF

El receptor de medios de ASF es el componente final de la canalización de codificación que permite a una aplicación escribir un archivo ASF.

Media Foundation proporciona dos tipos de receptores multimedia de ASF:

-   *El receptor de archivos ASF* se usa para archivar datos multimedia de ASF en un archivo.
-   *El receptor de streaming de ASF* se usa para escribir contenido de ASF en una secuencia de bytes que se puede transmitir a través de la red.

Los receptores multimedia de ASF contienen uno o varios receptores de flujo, que representa los datos que se escriben para cada secuencia en el archivo ASF de salida. Para codificar aplicaciones que se ejecutan en Windows Vista, debe configurar manualmente la topología de codificación mediante la creación y configuración del receptor de medios de ASF y, a continuación, agregarla a la topología. En Windows 7, si usa los objetos de transcodificación rápida para crear la topología, no tiene el receptor de medios directamente y la aplicación no llama a ningún método en el receptor de medios ni en ninguno de los receptores de flujo. Los objetos de transcodificación rápida crea una instancia de los receptores multimedia necesarios y lo agregan a la topología antes de devolver una referencia a la aplicación que llama. Sin embargo, para transcodificar objetos rápidamente, hay algunas restricciones que se aplican en función del tipo de codificación.

-   [Modelo de objetos receptores multimedia de ASF](#asf-media-sink-object-model)
-   [Receptor de archivos ASF](#asf-file-sink)
-   [Temas relacionados](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modelo de objetos receptores multimedia de ASF

Los receptores multimedia de ASF implementan la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) y exponen las interfaces siguientes. Una aplicación puede obtener una referencia a estas interfaces llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el receptor de medios de ASF que usa para generar ejemplos de salida.



| Interfaz                                                  | Descripción                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Necesario para todos los receptores de medios.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implementado por el receptor de archivos ASF que escribe el contenido multimedia generado en un archivo. Puede usar los métodos de esta interfaz para vaciar los datos y actualizar el objeto de encabezado ASF del archivo de salida final. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Recibe notificaciones de cambio de estado del reloj de presentación.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | El objeto ContentInfo de ASF es un objeto de nivel WMContainer que almacena principalmente la información del objeto de encabezado de ASF. Se usa para crear receptores de medios de ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Se usa para describir los metadatos del archivo ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Recupera una colección de metadatos, ya sea para una presentación completa o para una secuencia de la presentación.                                                                                          |



 

## <a name="asf-file-sink"></a>Receptor de archivos ASF

El receptor de archivos DE ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.

Debe crear, configurar y llamar a métodos en el receptor de archivos o en cualquiera de sus receptores de flujo si usa los objetos de capa de canalización para escribir un nuevo archivo ASF. Después de configurar el receptor de archivos, puede agregarlo a la canalización de codificación.

Estos son los pasos generales para usar el receptor de archivos ASF:

1.  Cree el receptor de archivos en proceso o fuera de proceso.
2.  Configure el receptor de archivos con todas las secuencias, propiedades de codificación e información de metadatos.
3.  Asocie el receptor de archivo con el nodo de topología de salida enumerando los receptores de flujo o haciendo un seguimiento de los números de flujo con en el receptor.

Los temas siguientes contienen información detallada sobre cómo trabajar con el receptor de archivos ASF:

-   [Creación del receptor de archivos ASF](creating-the-asf-file-sink.md)
-   [Adición de información de flujo al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md)
-   [Agregar metadatos al receptor de archivos](adding-metadata-to-the-file-sink.md)
-   [El modelo de búfer de cubo filtrada](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
