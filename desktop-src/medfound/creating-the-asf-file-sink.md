---
description: Obtenga información sobre cómo crear el receptor de archivos ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Creación del receptor de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ed3aeb3082277fa3a8bb4c814c1a82f92dd3da8815ffdbd70e4ef87d0d4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743263"
---
# <a name="creating-the-asf-file-sink"></a>Creación del receptor de archivos ASF

El receptor de archivos DE ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores multimedia de ASF.](asf-media-sinks.md)

Hay dos maneras de crear una instancia del receptor de archivos ASF. Puede llamar a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o [**MFCreateASFMediaSinkActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)

Si llama a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), debe especificar una secuencia de bytes, para el archivo de salida, en la que el receptor escribirá el contenido de ASF durante una sesión de codificación. La secuencia de bytes especificada debe tener funcionalidades que se pueden buscar y escribir; de lo contrario, se produce un error en la llamada **a MFCreateASFMediaSink** con el código de error E \_ FAIL. Esta llamada crea un objeto receptor de archivo en proceso y devuelve un puntero a la interfaz [**DEMMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de archivos.

Si llama a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), debe especificar la dirección URL del archivo de salida en el que el receptor del archivo escribirá datos multimedia. En este caso, el receptor de archivos crea internamente la secuencia de bytes. La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del receptor de archivos. En

Considere la posibilidad de usar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) en lugar de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)cuando la topología de codificación esté diseñada de la siguiente manera:

-   La topología de codificación es para la ruta de acceso multimedia protegida (PMP) y el receptor de archivos se usa fuera de proceso.
-   El nodo de salida de la topología se crea mediante el puntero devuelto al objeto activate del receptor de archivos y la aplicación realiza un seguimiento de las secuencias del receptor de archivos mediante números de secuencia.
    > [!Note]  
    > Puede activar el receptor de archivos mediante una llamada [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Sin embargo, no es necesario activar el objeto de forma explícita. La sesión multimedia realiza un seguimiento del objeto de activación y activa el receptor de archivos automáticamente durante la sesión de codificación.

     

-   La información de secuencia se configura en el objeto ContentInfo. Se ha desenlazado en la siguiente subsección.

Después de crear el receptor de archivos ASF, debe configurarse antes de compilar la topología. El receptor de archivos debe conocer la siguiente información para generar el archivo de salida.

-   Información básica del flujo
-   Información del modo de codificación
-   Metadatos

El receptor de archivos implementa el objeto ContentInfo de [ASF](asf-contentinfo-object.md) y expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) para que una aplicación pueda usarla para establecer información relacionada con las secuencias y la codificación. En función de la función a la que llamó para crear el receptor de archivos, hay dos maneras de obtener una referencia a la interfaz **IMFASFContentInfo.**

-   Si llama a la función [**MFCreateASFMediaSink,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) la aplicación debe consultar la interfaz [**MFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) llamando a **MFMediaSink::QueryInterface** en el receptor de archivos devuelto.
-   Si decide llamar a [**MFCreateASFMediaSinkActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)esta función espera que tenga un objeto ContentInfo totalmente configurado antes de la llamada. Para ello, debe crear un objeto ContentInfo vacío mediante una llamada a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) y, a continuación, configurarlo con toda la información necesaria. Pase el objeto ContentInfo configurado a **MFCreateASFMediaSinkActivate** para recibir un puntero al objeto de activación del receptor. No puede activar el receptor de archivos mediante el objeto de activación devuelto y, a continuación, cambiar cualquier transmisión o información de codificación.

Para obtener información sobre cómo configurar flujos receptores y propiedades específicas, vea los temas siguientes:

-   [Adición de información de flujo al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md)
-   [Agregar metadatos al receptor de archivos](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores multimedia de ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



