---
description: El receptor de archivos ASF es una implementación de IMFMediaSink proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios ASF y el uso general, consulte receptores multimedia ASF.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Crear el receptor de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43625bcbc581b4967d4db99cef71a0fc779f070
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153659"
---
# <a name="creating-the-asf-file-sink"></a>Crear el receptor de archivos ASF

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos y el uso general de los receptores de medios ASF, consulte [receptores de medios ASF](asf-media-sinks.md).

Hay dos formas de crear una instancia del receptor de archivos ASF. Puede llamar a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Si llama a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), debe especificar una secuencia de bytes, para el archivo de salida, en la que el receptor escribirá el contenido ASF durante una sesión de codificación. La secuencia de bytes especificada debe tener funcionalidades de búsqueda y escritura; de lo contrario, se produce un error en la llamada **MFCreateASFMediaSink** con el \_ código de error E Fail. Esta llamada crea un objeto de receptor de archivo en proceso y devuelve un puntero a la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de archivo.

Si llama a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), debe especificar la dirección URL del archivo de salida en el que el receptor de archivo escribirá los datos multimedia. En este caso, el receptor de archivo crea internamente la secuencia de bytes. La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del receptor de archivo. En

Considere la posibilidad de [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) en lugar de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), cuando la topología de codificación esté diseñada de la siguiente manera:

-   La topología de codificación es para la ruta de acceso a medios protegidos (PMP) y el receptor de archivos se usa fuera de proceso.
-   El nodo de salida de la topología se crea mediante el puntero devuelto al objeto activa del receptor de archivos y la aplicación realiza un seguimiento de las secuencias del receptor de archivos por números de secuencia.
    > [!Note]  
    > Puede activar el receptor de archivos llamando a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Sin embargo, no es necesario activar el objeto explícitamente. La sesión multimedia realiza un seguimiento del objeto de activación y activa el receptor de archivos automáticamente durante la sesión de codificación.

     

-   La información de la secuencia se configura en el objeto ContentInfo. Disucssed en la subsección siguiente.

Después de crear el receptor de archivo ASF, debe configurarlo antes de compilar la topología. El receptor de archivos necesita conocer la siguiente información para generar el archivo de salida.

-   Información básica de la secuencia
-   Información del modo de codificación
-   Metadatos

El receptor de archivos implementa el [objeto ContentInfo de ASF](asf-contentinfo-object.md) y expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) para que una aplicación pueda usarla para establecer información relacionada con las secuencias y la codificación. Dependiendo de la función a la que llamó para crear el receptor de archivos, hay dos maneras de obtener una referencia a la interfaz **IMFASFContentInfo** .

-   Si llama a la función [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) , la aplicación debe consultar la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) llamando a **IMFMediaSink:: QueryInterface** en el receptor de archivo devuelto.
-   Si decide llamar a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), esta función espera que tenga un objeto ContentInfo totalmente configurado antes de la llamada. Para ello, debe crear un objeto ContentInfo vacío llamando a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) y, a continuación, configurarlo con toda la información necesaria. Pase el objeto ContentInfo configurado a **MFCreateASFMediaSinkActivate** para recibir un puntero al objeto Sink Activate. No se puede activar el receptor de archivos mediante el objeto de activación devuelto y, a continuación, cambiar cualquier información de secuencia o codificación.

Para obtener información sobre la configuración de secuencias de receptor y propiedades específicas, vea los temas siguientes:

-   [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md)
-   [Agregar metadatos al receptor de archivos](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores de medios ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



