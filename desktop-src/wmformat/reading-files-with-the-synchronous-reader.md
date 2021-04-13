---
title: Leer archivos con el lector sincrónico
description: Leer archivos con el lector sincrónico
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- SDK de Windows Media Format, leer archivos
- SDK de Windows Media Format, lectores sincrónicos
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- lectores sincrónicos, interfaz IWMReaderCallback
- IWMReaderCallback, lectores sincrónicos
- lectores sincrónicos, leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420243"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Leer archivos con el lector sincrónico

Puede usar el lector sincrónico para leer un archivo ASF mediante llamadas sincrónicas en lugar de los métodos asincrónicos en el objeto Reader. El uso de llamadas sincrónicas reduce el número de subprocesos necesarios para leer un archivo. El lector asincrónico usa varios subprocesos para el procesamiento de secuencias. En el caso de los archivos con varias secuencias, el número de subprocesos utilizados puede llegar a ser muy grande. El lector sincrónico solo usa un subproceso.

El lector sincrónico se diseñó para satisfacer las necesidades de creación de contenido y aplicaciones de edición de archivos. Puede usar el lector sincrónico para otras aplicaciones, pero su funcionalidad es limitada.

El lector sincrónico puede abrir archivos que son locales o archivos en una red mediante el nombre de la ruta de acceso UNC (por ejemplo, " \\ \\ someshare \\ somedirectory \\ somefile. WMV"). No se pueden transmitir archivos al lector sincrónico ni abrir archivos desde una ubicación de Internet. El lector sincrónico también proporciona compatibilidad para utilizar la interfaz com de **IStream** como origen.

El lector sincrónico proporciona más versatilidad para recuperar ejemplos de un archivo ASF que el lector asincrónico. El lector sincrónico puede proporcionar ejemplos por número de secuencia y por salida. Los ejemplos proporcionados por el número de secuencia se pueden comprimir o descomprimir. El lector sincrónico también puede cambiar entre la entrega comprimida y sin comprimir durante la reproducción. Esta característica se conoce como "edición rápida". Esta característica permite a una aplicación de edición leer contenido basado en Windows Media y pasarlo directamente al escritor hasta que se alcance un fotograma deseado. En ese momento, la aplicación puede indicar al lector que comience a entregar contenido sin comprimir, que la aplicación puede modificar y pasar al escritor para volver a comprimirlo. Cuando la aplicación haya terminado de modificar los fotogramas especificados, puede indicar al lector que empiece a entregar fotogramas comprimidos de nuevo.

La funcionalidad más básica del objeto lector sincrónico se puede desglosar en los pasos siguientes. En estos pasos "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.

1.  La aplicación pasa al lector sincrónico el nombre de un archivo que se va a leer. Cuando el lector sincrónico abre el archivo, asigna un número de salida a cada flujo. Si el archivo usa exclusión mutua, el lector asigna una salida única para todos los flujos mutuamente excluyentes.
2.  La aplicación obtiene información sobre la configuración de las distintas salidas del lector. La información recopilada permitirá a la aplicación representar correctamente los ejemplos de medios.
3.  La aplicación comienza a solicitar muestras, de una en una, del lector sincrónico. El lector sincrónico entrega cada ejemplo en un objeto de búfer para el que entrega la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .
4.  La aplicación es responsable de representar los datos después de que los entregue el lector. El SDK de Windows Media Format no proporciona ninguna rutina de representación. Normalmente, las aplicaciones usarán otros SDK para representar datos, como el SDK de Microsoft Direct X o las funciones multimedia del SDK de la plataforma Microsoft Windows.

Estos pasos se ilustran en la aplicación de ejemplo WMSyncReader. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

El lector sincrónico también admite una funcionalidad más avanzada. El lector sincrónico le permite hacer lo siguiente:

-   Especifique un intervalo de muestras para recuperar por hora o por número de marco.
-   Control de la selección de flujo para flujos mutuamente excluyentes.
-   Abra un archivo mediante la interfaz COM estándar, **IStream**.
-   Leer los datos de perfil del encabezado de archivo.
-   Leer metadatos del encabezado de archivo.
-   Cambiar entre los ejemplos de flujo y salida durante la reproducción.
-   Cambiar entre los ejemplos de secuencias comprimidas y sin comprimir durante la reproducción.

En las secciones siguientes se describe detalladamente el uso del objeto de lector sincrónico.

-   [Para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Para buscar números de secuencia y números de salida](to-find-stream-numbers-and-output-numbers.md)
-   [Para recuperar ejemplos de medios con el lector sincrónico](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Para buscar por tiempo mediante el lector sincrónico](to-seek-by-time-using-the-synchronous-reader.md)
-   [Para buscar por número de marco mediante el lector sincrónico](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Para buscar por el código de tiempo de SMPTE mediante el lector sincrónico](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Para recuperar ejemplos de secuencias con el lector sincrónico](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Para recuperar muestras comprimidas con el lector sincrónico](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Código de ejemplo**

En el ejemplo de código siguiente se muestra cómo leer ejemplos de un archivo ASF mediante el lector sincrónico. Especifica por el número de marco un intervalo de muestras que se van a proporcionar.


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

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> </dl>

 

 




