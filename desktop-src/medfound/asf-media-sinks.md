---
description: El receptor de medios ASF es el último componente de la canalización de codificación que permite que una aplicación escriba un archivo ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Receptores de medios ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678645"
---
# <a name="asf-media-sinks"></a>Receptores de medios ASF

El receptor de medios ASF es el último componente de la canalización de codificación que permite que una aplicación escriba un archivo ASF.

Media Foundation proporciona dos tipos de receptores de medios ASF:

-   El *receptor de archivos ASF* se usa para archivar los datos multimedia ASF en un archivo.
-   El *receptor de streaming ASF* se utiliza para escribir contenido ASF en una secuencia de bytes que se puede transmitir por secuencias a través de la red.

Los receptores de medios ASF contienen uno o varios receptores de secuencias, que representan los datos que se van a escribir para cada flujo en el archivo ASF de salida. En el caso de las aplicaciones de codificación que se ejecutan en Windows Vista, debe configurar manualmente la topología de codificación creando y configurando el receptor de medios ASF y agregándolo a la topología. En Windows 7, si usa los objetos de transcodificación rápida para crear la topología, no tiene que crear el receptor de medios directamente y la aplicación no llama a ningún método en el receptor de medios ni en ninguno de los receptores de flujo. Los objetos de transcodificación rápida crean instancias de los receptores de medios necesarios y lo agregan a la topología antes de devolver una referencia a la aplicación del llamador. Sin embargo, en el caso de los objetos de transcodificación rápida, existen algunas restricciones que se aplican en función del tipo de codificación.

-   [Modelo de objetos de receptor multimedia ASF](#asf-media-sink-object-model)
-   [Receptor de archivos ASF](#asf-file-sink)
-   [Temas relacionados](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modelo de objetos de receptor multimedia ASF

Los receptores de medios ASF implementan la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) y exponen las interfaces siguientes. Una aplicación puede obtener una referencia a estas interfaces llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el receptor de medios de ASF que se usa para generar ejemplos de salida.



| Interfaz                                                  | Descripción                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Se requiere para todos los receptores de medios.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implementado por el receptor de archivos ASF que escribe el contenido multimedia generado en un archivo. Puede usar los métodos de esta interfaz para vaciar los datos y actualizar el objeto de encabezado ASF del archivo de salida final. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Recibe notificaciones de cambio de estado del reloj de presentación.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | El objeto ASF ContentInfo es un objeto de nivel WMContainer que almacena principalmente información del objeto de encabezado ASF. Se utiliza para crear receptores de medios ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Se utiliza para describir los metadatos del archivo ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Recupera una colección de metadatos, ya sea para una presentación completa o para un flujo en la presentación.                                                                                          |



 

## <a name="asf-file-sink"></a>Receptor de archivos ASF

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo.

Debe crear, configurar y llamar a métodos en el receptor de archivos o cualquiera de sus receptores de flujo Si usa los objetos de capa de canalización para escribir un nuevo archivo ASF. Después de configurar el receptor de archivos, puede agregarlo a la canalización de codificación.

Estos son los pasos generales para usar el receptor de archivos ASF:

1.  Cree el receptor de archivos en proceso o fuera de proceso.
2.  Configure el receptor de archivos con todos los flujos, propiedades de codificación e información de metadatos.
3.  Asocie el receptor de archivos al nodo de la topología de salida; para ello, enumere los receptores de flujo o realice un seguimiento de los números de flujo con en el receptor.

Los temas siguientes contienen información detallada sobre cómo trabajar con el receptor de archivos ASF:

-   [Crear el receptor de archivos ASF](creating-the-asf-file-sink.md)
-   [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md)
-   [Agregar metadatos al receptor de archivos](adding-metadata-to-the-file-sink.md)
-   [El modelo de búfer de depósito con fugas](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
