---
title: Trabajar con receptores de escritor
description: Trabajar con receptores de escritor
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), receptores de escritor
- ASF (formato de sistemas avanzados), receptores de escritor
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores de escritor
- receptores de escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788667"
---
# <a name="working-with-writer-sinks"></a>Trabajar con receptores de escritor

El objeto de escritor del SDK de Windows Media Format procesa los datos de los medios de entrada en un flujo de bits. Sin embargo, el objeto de escritor no entrega el flujo de bits a su destino final (ya sea a un archivo o a una ubicación de red). Para escribir el contenido ASF en un formato utilizable, debe utilizar receptores de escritor.

El objeto de escritor admite tres tipos de receptores: receptores de archivos, receptores de red y receptores de envío. Un receptor de archivos escribe el contenido ASF en un archivo ASF en disco. Un receptor de red difunde el contenido ASF de una dirección de red. Un receptor de inserciones envía datos a un servidor que ejecuta Windows Media Services para que el servidor pueda hacer que el contenido esté disponible para el público previsto. También puede crear sus propios receptores para proporcionar datos ASF de la forma que necesite la aplicación. Para obtener información acerca de los receptores de red y los receptores de envío, consulte [envío de datos ASF a través de una red](sending-asf-data-over-a-network.md). En el resto de esta sección se describen los receptores de escritor.

Puede configurar uno o varios receptores para cada instancia del escritor que use. Cada receptor solo controla un destino. Por ejemplo, si desea escribir tres archivos a la vez, debe crear y configurar un receptor de archivos independiente para cada uno.

En las secciones siguientes se describe el uso de receptores de escritor.



| Sección                                                                      | Descripción                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Agregar receptores al escritor](adding-sinks-to-the-writer.md)                 | Describe cómo agregar receptores al escritor.                                        |
| [Enumerar receptores](enumerating-sinks.md)                                   | Describe cómo enumerar los receptores que se han agregado al escritor.         |
| [Obtener mensajes de error de un receptor](getting-error-messages-from-a-sink.md) | Describe cómo configurar receptores para proporcionar mensajes de estado a la aplicación. |
| [Uso de receptores de archivos](using-file-sinks.md)                                     | Describe cómo usar un receptor de archivos de escritor para crear un archivo ASF en disco.           |
| [Usar receptores personalizados](using-custom-sinks.md)                                 | Describe cómo crear y usar sus propios receptores personalizados para proporcionar datos ASF.       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaz IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




