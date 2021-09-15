---
title: Trabajar con receptores de escritor
description: Trabajar con receptores de escritor
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Formato de sistemas avanzados (ASF), receptores de escritor
- ASF (formato de sistemas avanzados), receptores de escritor
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- sinks,writer sinks
- receptores de escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466202"
---
# <a name="working-with-writer-sinks"></a>Trabajar con receptores de escritor

El objeto de escritor del SDK Windows Media Format procesa los datos multimedia de entrada en una secuencia de bits. Sin embargo, el objeto de escritor no entrega la secuencia de bits a su destino final (ya sea a un archivo o a una ubicación de red). Para escribir el contenido de ASF en un formato utilizable, debe usar receptores de escritor.

El objeto de escritor admite tres tipos de receptores: receptores de archivos, receptores de red y receptores de inserción. Un receptor de archivos escribe contenido de ASF en un archivo ASF en el disco. Un receptor de red difunde el contenido de ASF desde una dirección de red. Un receptor de inserción entrega datos a un servidor que Servicios de Windows Media para que el servidor pueda hacer que el contenido esté disponible para su público previsto. También puede crear sus propios receptores para entregar datos de ASF de la manera que requiera la aplicación. Para obtener información sobre los receptores de red y los receptores de inserción, consulte Envío de datos [de ASF a través de una red.](sending-asf-data-over-a-network.md) En el resto de esta sección se deba a los receptores de escritor.

Puede configurar uno o varios receptores para cada instancia del escritor que use. Cada receptor controla solo un destino. Por ejemplo, si desea escribir tres archivos a la vez, debe crear y configurar un receptor de archivos independiente para cada uno.

En las secciones siguientes se describe el uso de receptores de escritor.



| Sección                                                                      | Descripción                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Agregar receptores al escritor](adding-sinks-to-the-writer.md)                 | Describe cómo agregar receptores al sistema de escritura.                                        |
| [Enumeración de receptores](enumerating-sinks.md)                                   | Describe cómo enumerar los receptores que se han agregado al sistema de escritura.         |
| [Obtener mensajes de error de un receptor](getting-error-messages-from-a-sink.md) | Describe cómo configurar receptores para entregar mensajes de estado a la aplicación. |
| [Uso de receptores de archivos](using-file-sinks.md)                                     | Describe cómo usar un receptor de archivos de escritor para crear un archivo ASF en el disco.           |
| [Uso de receptores personalizados](using-custom-sinks.md)                                 | Describe cómo crear y usar sus propios receptores personalizados para entregar datos de ASF.       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterSink (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




