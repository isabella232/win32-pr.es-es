---
title: Leer archivos con el lector asincrónico
description: Leer archivos con el lector asincrónico
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- SDK de Windows Media Format, leer archivos
- SDK de Windows Media Format, lectores asincrónicos
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- lectores asincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback, lectores asincrónicos
- lectores asincrónicos, leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420244"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Leer archivos con el lector asincrónico

El lector asincrónico lee el contenido de los archivos ASF mediante varios subprocesos y llamadas asincrónicas. Las características admitidas por el lector asincrónico hacen que sea adecuado para las aplicaciones que presentan contenido a los usuarios finales.

La funcionalidad más básica del objeto lector se puede desglosar en los pasos siguientes. En estos pasos "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.

1.  La aplicación implementa la interfaz [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para controlar los mensajes del lector. Esto incluye dos métodos de devolución de llamada: **Alstatus**, que recibe mensajes relacionados con el estado de diversos aspectos del lector y el **ejemplo**, que recibe muestras sin comprimir del lector.
2.  La aplicación pasa al lector el nombre de un archivo que se va a leer. Cuando el lector abre el archivo, asigna un número de salida a cada flujo. Si el archivo usa exclusión mutua, el lector asigna una salida única para todos los flujos mutuamente excluyentes.
3.  La aplicación obtiene información sobre la configuración de las distintas salidas del lector. La información recopilada permitirá a la aplicación representar correctamente los ejemplos de medios.
4.  La aplicación indica al lector que empiece a leer los datos del archivo. El lector comienza a entregar muestras sin comprimir a la devolución de llamada de **ejemplo** de una en una en los búferes encapsulados en los objetos de búfer. Los ejemplos proporcionados por el lector están en el orden en tiempo de presentación. El lector seguirá entregando muestras hasta que la aplicación la detenga o hasta que se alcance el final del archivo.
5.  La aplicación es responsable de representar los datos después de que los entregue el lector. El SDK de Windows Media Format no proporciona ninguna rutina de representación. Normalmente, las aplicaciones usarán otros SDK para representar datos, como Microsoft DirectX® SDK o las funciones multimedia del SDK de la plataforma Microsoft Windows.
6.  Cuando se completa la lectura, la aplicación indica al lector que cierre el archivo.

Estos pasos se muestran en la aplicación de ejemplo AudioPlayer, entre otros. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

El lector también admite una funcionalidad más avanzada. El lector le permite hacer lo siguiente:

-   Pausar la reproducción de un archivo.
-   Recupera las estadísticas de rendimiento del lector.
-   Control de la selección de flujo para flujos mutuamente excluyentes.
-   Asignación manual de búferes para la salida.
-   Proporcione su propio reloj.
-   Recuperar el estado de las operaciones de archivo (almacenamiento en búfer, descarga o guardado).
-   Abra un archivo mediante la interfaz COM estándar, **IStream**.
-   Buscar puntos específicos en un archivo ASF.
-   Leer los datos de perfil del encabezado del archivo.

En las secciones siguientes se describe detalladamente el uso del objeto Reader.

-   [Para implementar mensajes de lector en la devolución de llamada de estado](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Para implementar la devolución de llamada de ejemplo](to-implement-the-onsample-callback.md)
-   [Para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md)
-   [Para recuperar ejemplos de medios con el lector asincrónico](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Para buscar por tiempo mediante el lector asincrónico](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Para buscar por número de marco mediante el lector asincrónico](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Para buscar por el código de tiempo de SMPTE mediante el lector asincrónico](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Para buscar marcadores](to-seek-to-markers.md)
-   [Para pausar o detener la reproducción](to-pause-or-stop-playback.md)
-   [Para obtener las estadísticas de rendimiento del lector](to-get-reader-performance-statistics.md)
-   [Para usar la selección de flujo manual](to-use-manual-stream-selection.md)
-   [Para proporcionar ejemplos comprimidos con el lector asincrónico](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> </dl>

 

 




