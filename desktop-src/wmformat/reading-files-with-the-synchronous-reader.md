---
title: Lectura de archivos con el lector sincrónico
description: Lectura de archivos con el lector sincrónico
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows SDK de formato multimedia, lectura de archivos
- Windows SDK de formato multimedia, lectores sincrónicos
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Formato de sistemas avanzados (ASF), lectura de archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- lectores sincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback,lectores sincrónicos
- lectores sincrónicos, lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466665"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lectura de archivos con el lector sincrónico

Puede usar el lector sincrónico para leer un archivo ASF mediante llamadas sincrónicas en lugar de los métodos asincrónicos en el objeto reader. El uso de llamadas sincrónicas reduce el número de subprocesos necesarios para leer un archivo. El lector asincrónico usa varios subprocesos para procesar secuencias. En el caso de los archivos con varias secuencias, el número de subprocesos usados puede ser muy grande. El lector sincrónico solo usa un subproceso.

El lector sincrónico se diseñó para satisfacer las necesidades de las aplicaciones de creación de contenido y edición de archivos. Puede usar el lector sincrónico para otras aplicaciones, pero su funcionalidad es limitada.

El lector sincrónico puede abrir archivos locales o archivos en una red mediante el nombre de ruta de acceso UNC (por ejemplo, \\ \\ "someshare \\ somedirectory \\ somefile.wmv"). No se pueden transmitir archivos al lector sincrónico ni abrir archivos desde una ubicación de Internet. El lector sincrónico también proporciona compatibilidad para usar la interfaz COM **IStream** como origen.

El lector sincrónico proporciona más flexibilidad para recuperar ejemplos de un archivo ASF que el lector asincrónico. El lector sincrónico puede entregar ejemplos por número de secuencia, así como por salida. Los ejemplos entregados por número de secuencia se pueden comprimir o descomprimir. El lector sincrónico también puede cambiar entre la entrega comprimida y la sin comprimir durante la reproducción. esta característica se conoce como "edición rápida". Esta característica permite a una aplicación de edición leer Windows contenido basado en multimedia y pasarlo directamente al escritor hasta que se alcance un marco deseado. En ese momento, la aplicación puede decir al lector que empiece a entregar contenido sin comprimir, que la aplicación puede modificar y pasar al escritor para su recompresión. Cuando la aplicación haya terminado de modificar los fotogramas especificados, puede decir al lector que empiece a entregar fotogramas comprimidos de nuevo.

La funcionalidad más básica del objeto de lector sincrónico se puede dividir en los pasos siguientes. En estos pasos , "la aplicación" hace referencia al programa que escribe mediante el SDK Windows Media Format.

1.  La aplicación pasa al lector sincrónico el nombre de un archivo que se leerá. Cuando el lector sincrónico abre el archivo, asigna un número de salida a cada secuencia. Si el archivo usa la exclusión mutua, el lector asigna una única salida para todas las secuencias mutuamente excluyentes.
2.  La aplicación obtiene información sobre la configuración de las distintas salidas del lector. La información recopilada permitirá que la aplicación represente correctamente ejemplos multimedia.
3.  La aplicación comienza a solicitar ejemplos, de uno en uno, desde el lector sincrónico. El lector sincrónico entrega cada muestra en un objeto de búfer para el que entrega la [**interfaz INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
4.  La aplicación es responsable de representar los datos una vez entregados por el lector. El SDK Windows Media Format no proporciona ninguna rutina de representación. Normalmente, las aplicaciones usarán otros SDK para representar datos, como el SDK de Microsoft Direct X o las funciones multimedia de Microsoft Windows Platform SDK.

Estos pasos se ilustran en la aplicación de ejemplo WMSyncReader. Para obtener más información, vea [Aplicaciones de ejemplo.](sample-applications.md)

El lector sincrónico también admite funcionalidades más avanzadas. El lector sincrónico permite hacer lo siguiente:

-   Especifique un intervalo de muestras para recuperar por hora o por número de fotograma.
-   Controlar la selección de secuencias para secuencias mutuamente excluyentes.
-   Abra un archivo mediante la interfaz COM estándar, **IStream**.
-   Lee los datos del perfil del encabezado de archivo.
-   Lee los metadatos del encabezado de archivo.
-   Cambie entre los ejemplos de secuencia y salida durante la reproducción.
-   Cambie entre muestras de secuencias comprimidas y sin comprimir durante la reproducción.

En las secciones siguientes se describe el uso del objeto de lector sincrónico en detalle.

-   [Para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Para buscar números de flujo y números de salida](to-find-stream-numbers-and-output-numbers.md)
-   [Para recuperar ejemplos de medios con el lector sincrónico](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Para buscar por tiempo mediante el lector sincrónico](to-seek-by-time-using-the-synchronous-reader.md)
-   [Para buscar por número de fotograma mediante el lector sincrónico](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Para buscar por código de tiempo SMPTE mediante el lector sincrónico](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Para recuperar ejemplos de secuencia con el lector sincrónico](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Para recuperar ejemplos comprimidos con el lector sincrónico](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Código de ejemplo**

En el código de ejemplo siguiente se muestra cómo leer ejemplos de un archivo ASF mediante el lector sincrónico. Especifica por número de fotograma un intervalo de muestras que se van a entregar.


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> </dl>

 

 




