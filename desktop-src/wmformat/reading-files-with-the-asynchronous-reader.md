---
title: Leer archivos con el lector asincrónico
description: Leer archivos con el lector asincrónico
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows SDK de formato multimedia, lectura de archivos
- Windows SDK de formato multimedia, lectores asincrónicos
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), leer archivos
- ASF (formato de sistemas avanzados), leer archivos
- lectores asincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback,lectores asincrónicos
- lectores asincrónicos, leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466667"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Leer archivos con el lector asincrónico

El lector asincrónico lee el contenido de los archivos ASF mediante varios subprocesos y llamadas asincrónicas. Las características admitidas por el lector asincrónico hacen que sea adecuada para las aplicaciones que representan contenido a los usuarios finales.

La funcionalidad más básica del objeto de lector se puede dividir en los pasos siguientes. En estos pasos, "la aplicación" hace referencia al programa que escribe con el SDK Windows Media Format.

1.  La aplicación implementa la interfaz [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) para controlar los mensajes del lector. Esto incluye dos métodos de devolución de llamada: **OnStatus**, que recibe mensajes relacionados con el estado de varios aspectos del lector y **OnSample**, que recibe muestras sin comprimir del lector.
2.  La aplicación pasa al lector el nombre de un archivo que se leerá. Cuando el lector abre el archivo, asigna un número de salida a cada secuencia. Si el archivo usa la exclusión mutua, el lector asigna una única salida para todas las secuencias mutuamente excluyentes.
3.  La aplicación obtiene información sobre la configuración de las distintas salidas del lector. La información recopilada permitirá que la aplicación represente correctamente ejemplos multimedia.
4.  La aplicación indica al lector que comience a leer datos del archivo. El lector comienza a entregar muestras sin comprimir a la devolución de llamada **OnSample** de una en una en búferes encapsulados en objetos de búfer. Los ejemplos entregados por el lector están en orden de presentación. El lector seguirá entregando ejemplos hasta que la aplicación lo detenga o hasta que se alcance el final del archivo.
5.  La aplicación es responsable de representar los datos una vez entregados por el lector. El SDK Windows media format no proporciona ninguna rutina de representación. Normalmente, las aplicaciones usarán otros SDK para representar datos, como el SDK de Microsoft DirectX® o las funciones multimedia del SDK de plataforma de Windows Microsoft.
6.  Una vez completada la lectura, la aplicación indica al lector que cierre el archivo.

Estos pasos se muestran en la aplicación de ejemplo AudioPlayer, entre otros. Para obtener más información, vea [Aplicaciones de ejemplo.](sample-applications.md)

El lector también admite una funcionalidad más avanzada. El lector le permite hacer lo siguiente:

-   Pausar la reproducción de un archivo.
-   Recuperar estadísticas de rendimiento del lector.
-   Controlar la selección de secuencias para secuencias mutuamente excluyentes.
-   Asignar manualmente búferes para la salida.
-   Proporcione su propio reloj.
-   Recupere el estado de las operaciones de archivo (almacenamiento en búfer, descarga o guardado).
-   Abra un archivo mediante la interfaz COM estándar, **IStream**.
-   Busque puntos específicos en un archivo ASF.
-   Lee los datos del perfil del encabezado del archivo.

En las secciones siguientes se describe detalladamente el uso del objeto de lector.

-   [Para implementar mensajes de lector en la devolución de llamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Para implementar la devolución de llamada OnSample](to-implement-the-onsample-callback.md)
-   [Para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md)
-   [Para recuperar ejemplos de medios con el lector asincrónico](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Para buscar por tiempo mediante el lector asincrónico](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Para buscar por número de fotograma mediante el lector asincrónico](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Para buscar por código de tiempo de SMPTE mediante el lector asincrónico](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Para buscar marcadores](to-seek-to-markers.md)
-   [Para pausar o detener la reproducción](to-pause-or-stop-playback.md)
-   [Para obtener estadísticas de rendimiento del lector](to-get-reader-performance-statistics.md)
-   [Para usar la selección manual de secuencias](to-use-manual-stream-selection.md)
-   [Para entregar ejemplos comprimidos con el lector asincrónico](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> </dl>

 

 




