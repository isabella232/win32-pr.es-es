---
title: Uso de receptores de archivos
description: Uso de receptores de archivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Formato de sistemas avanzados (ASF), receptores de archivo
- ASF (formato de sistemas avanzados), receptores de archivo
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores de archivo
- receptores de archivos, acerca de
- receptores de archivos, crear
- receptores de archivos, detener
- receptores de archivos, Inicio
- receptores de archivos, cerrar
- receptores, estadísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149125"
---
# <a name="using-file-sinks"></a>Uso de receptores de archivos

En circunstancias normales, puede simplemente pasar el escritor a un nombre de archivo de salida con el método [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) y el objeto de escritor escribirá el archivo en el disco automáticamente. En este caso, el escritor crea y controla realmente un objeto de receptor de archivos de escritor que controla la escritura del archivo en el disco. Un objeto de receptor de archivo de escritor controla el flujo de datos desde el objeto de escritor a un único archivo.

Puede crear sus propios receptores de archivos para obtener más control sobre cómo el receptor escribe el archivo. También puede tener acceso al receptor del archivo de escritura predeterminado creado por el escritor en respuesta a una llamada a **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Crear receptores de archivo

Para crear un receptor de archivos y agregarlo al escritor, realice los pasos siguientes.

1.  Cree un nuevo receptor mediante una llamada a la función [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .
2.  Proporcione un nombre de archivo para el receptor mediante una llamada a [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Agregue el receptor de archivos al escritor llamando a [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Realizar la escritura de la manera habitual.
5.  Una vez completada la escritura, el receptor cerrará automáticamente el archivo.

## <a name="stopping-and-starting-file-sinks"></a>Detención e inicio de los receptores de archivo

Una vez iniciada la operación de escritura, puede dejar de escribir en un receptor de archivos llamando a [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Hay muchas razones posibles por las que podría querer dejar de escribir en un receptor. Por ejemplo, si va a grabar desde un origen en directo, es posible que solo esté interesado en parte del contenido.

Puede reanudar la escritura en un receptor de archivos llamando a [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Las opciones **detener** e **iniciar** usan los tiempos de presentación para controlar aproximadamente el momento en que se ejecuta el comando. Puede usar los métodos [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obtener más control sobre las horas de inicio y detención.

## <a name="closing-file-sinks"></a>Cerrar los receptores de archivo

Normalmente, un receptor de archivo se cierra automáticamente. Si ha terminado de escribir en un receptor, pero la escritura de operaciones en otros receptores continúa, debe cerrar explícitamente el receptor para conservar los recursos. Para cerrar un receptor de archivos, llame a [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Obtención de estadísticas de receptor

Puede obtener el tamaño de archivo y la duración de un receptor abierto llamando a [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) y [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) , respectivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**Interfaz IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**Interfaz IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Objeto receptor de archivos de Writer**](writer-file-sink-object.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




