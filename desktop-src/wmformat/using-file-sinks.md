---
title: Uso de receptores de archivos
description: Uso de receptores de archivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Formato de sistemas avanzados (ASF), receptores de archivos
- ASF (formato de sistemas avanzados), receptores de archivos
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- sinks,file sinks
- receptores de archivos, acerca de
- receptores de archivos, crear
- receptores de archivos, deteniendo
- receptores de archivos, iniciar
- receptores de archivos, cierre
- sinks,statistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f94bd6698ca30a645957da36cf3b81a84f9d3e7c8ce6c598be2c39f8ac766db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196178"
---
# <a name="using-file-sinks"></a>Uso de receptores de archivos

En circunstancias normales, simplemente puede pasar al escritor un nombre de archivo de salida mediante el método [**IWMWriter::SetOutputFilename,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) y el objeto writer escribirá el archivo en el disco automáticamente. En este caso, el escritor crea y controla realmente un objeto receptor de archivo de escritura que controla la escritura del archivo en el disco. Un objeto receptor de archivo de escritor controla el flujo de datos del objeto de escritor a un único archivo.

Puede crear sus propios receptores de archivos para obtener más control sobre cómo escribe el archivo el receptor. También puede acceder al receptor de archivos de escritor predeterminado creado por el escritor en respuesta a una llamada a **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Creación de receptores de archivos

Para crear un receptor de archivos y agregarlo al escritor, realice los pasos siguientes.

1.  Cree un nuevo receptor mediante una llamada a la [**función WMCreateWriterFileSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
2.  Proporcione un nombre de archivo para el receptor mediante una [**llamada a IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Agregue el receptor de archivos al escritor mediante una [**llamada a IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Realice la escritura de la manera habitual.
5.  Una vez completada la escritura, el receptor cerrará el archivo automáticamente.

## <a name="stopping-and-starting-file-sinks"></a>Detención e inicio de receptores de archivos

Después de comenzar las operaciones de escritura, puede dejar de escribir en un receptor de archivos llamando a [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Hay muchas razones posibles por las que le gustaría dejar de escribir en un receptor. Por ejemplo, si está grabando desde un origen en directo, es posible que solo le interese parte del contenido.

Puede reanudar la escritura en un receptor de archivos llamando a [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Tanto **Stop** como **Start usan tiempos** de presentación para controlar aproximadamente cuándo se ejecuta el comando. Puede usar los métodos [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obtener más control sobre los tiempos de inicio y de detección.

## <a name="closing-file-sinks"></a>Receptores de archivos de cierre

Normalmente, un receptor de archivos se cierra automáticamente. Si ha terminado de escribir en un receptor, pero las operaciones de escritura en otros receptores continúan, debe cerrar explícitamente el receptor para conservar los recursos. Para cerrar un receptor de archivos, llame [**a IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Obtención de estadísticas de receptor

Puede obtener el tamaño de archivo y la duración de un receptor abierto llamando a [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2::GetFileDuration,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterFileSink (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**IWMWriterFileSink2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**IWMWriterFileSink3 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Objeto receptor de archivos de Writer**](writer-file-sink-object.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




