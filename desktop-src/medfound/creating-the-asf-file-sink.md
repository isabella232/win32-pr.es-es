---
description: Obtenga información sobre cómo crear el receptor de archivos de ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Creación del receptor de archivos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fcd9ea19f0200dfd330f421fd5dac2cd100b702
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360712"
---
# <a name="creating-the-asf-file-sink"></a>Creación del receptor de archivos de ASF

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores de medios de ASF.](asf-media-sinks.md)

Hay dos maneras de crear una instancia del receptor de archivos de ASF. Puede llamar a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Si llama a [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), debe especificar una secuencia de bytes para el archivo de salida, en la que el receptor escribirá el contenido de ASF durante una sesión de codificación. La secuencia de bytes especificada debe tener funcionalidades que se pueden buscar y escribir; de lo contrario, la llamada **MFCreateASFMediaSink** produce un error con el código de error E \_ FAIL. Esta llamada crea un objeto receptor de archivo en proceso y devuelve un puntero a la interfaz [**DEFMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del receptor de archivos.

Si llama a [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), debe especificar la dirección URL del archivo de salida en el que el receptor de archivos escribirá datos multimedia. En este caso, el receptor de archivos crea internamente la secuencia de bytes. La función devuelve un puntero a la interfaz [**DEFACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) del receptor de archivos. En

Considere la posibilidad de usar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) en lugar de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)cuando la topología de codificación esté diseñada de la siguiente manera:

-   La topología de codificación es para la ruta de acceso multimedia protegida (PMP) y el receptor de archivos se usa fuera de proceso.
-   El nodo de salida de la topología se crea mediante el puntero devuelto al objeto activate del receptor de archivos y la aplicación realiza un seguimiento de las secuencias del receptor de archivos mediante números de secuencia.
    > [!Note]  
    > Puede activar el receptor de archivos llamando [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Sin embargo, no es necesario activar el objeto de forma explícita. La sesión multimedia realiza un seguimiento del objeto de activación y activa automáticamente el receptor de archivos durante la sesión de codificación.

     

-   La información de flujo se configura en el objeto ContentInfo. Se muestra en la siguiente subsección.

Después de crear el receptor de archivos de ASF, debe configurarse antes de compilar la topología. El receptor del archivo debe conocer la siguiente información para generar el archivo de salida.

-   Información básica del flujo
-   Información del modo de codificación
-   Metadatos

El receptor de archivos implementa el objeto ContentInfo de [ASF](asf-contentinfo-object.md) y expone la interfaz [**DEFFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) para que una aplicación pueda usarla para establecer información relacionada con las secuencias y la codificación. En función de la función a la que llamó para crear el receptor de archivos, hay dos maneras de obtener una referencia a la interfaz **IMFASFContentInfo.**

-   Si llama a la función [**MFCreateASFMediaSink,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) la aplicación debe consultar la interfaz [**MFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) llamando a **MFMediaSink::QueryInterface** en el receptor de archivos devuelto.
-   Si decide llamar a [**MFCreateASFMediaSinkActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)esta función espera que tenga un objeto ContentInfo completamente configurado antes de la llamada. Para ello, debe crear un objeto ContentInfo vacío mediante una llamada a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) y, a continuación, configurarlo con toda la información necesaria. Pase el objeto ContentInfo configurado a **MFCreateASFMediaSinkActivate** para recibir un puntero al objeto de activación del receptor. No se puede activar el receptor de archivos mediante el objeto de activación devuelto y, a continuación, cambiar la información de transmisión o codificación.

Para obtener información sobre cómo configurar flujos receptores y propiedades específicas, vea los temas siguientes:

-   [Agregar información de flujo al receptor de archivos de ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md)
-   [Agregar metadatos al receptor de archivos](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores de medios de ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



