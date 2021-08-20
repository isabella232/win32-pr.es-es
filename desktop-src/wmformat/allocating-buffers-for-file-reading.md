---
title: Asignación de búferes para la lectura de archivos
description: Asignación de búferes para la lectura de archivos
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows SDK de formato multimedia, lectura de archivos ASF
- Formato de sistemas avanzados (ASF), leer archivos
- ASF (formato de sistemas avanzados), leer archivos
- Windows SDK de formato multimedia, asignación de búferes
- Formato de sistemas avanzados (ASF), asignación de búferes
- ASF (formato de sistemas avanzados), asignación de búferes
- Formato de sistemas avanzados (ASF), asignación de búfer
- ASF (formato de sistemas avanzados), asignación de búfer
- asignación de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c02f82cdeb19adb42c3240abb9b560a1fd2d86f3de3de3ac66d6930e43a57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656243"
---
# <a name="allocating-buffers-for-file-reading"></a>Asignación de búferes para la lectura de archivos

En el escenario de lectura de archivos más básico, el objeto de lectura (el objeto lector o el objeto de lector sincrónico) asigna los búferes usados para entregar ejemplos. Sin embargo, puede asignar búferes usted mismo. Para obtener más información sobre las ventajas de asignar sus propios búferes, vea Compatibilidad con ejemplos [asignados por el usuario.](user-allocated-sample-support.md)

Para usar sus propios búferes para la lectura de archivos, realice los pasos siguientes.

1.  Implemente una devolución de llamada o devoluciones de llamada para que el lector llame a cuando necesite un búfer. Si está leyendo ejemplos de salida, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Si está leyendo ejemplos de secuencias, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Incluya cualquier lógica para administrar los búferes que se adapten a la aplicación.
2.  Asigne un grupo de búferes que usará para la lectura de archivos.
    -   Busque el tamaño necesario para los búferes llamando a [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) o [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) para cada salida o secuencia para la que se usa el búfer. Si usa el lector sincrónico, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) o [**IWMSyncReader::GetMaxStreamSampleSize en su**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) lugar.
    -   Cree cada búfer para el grupo.
3.  Configure el lector o el lector sincrónico para la lectura. Para obtener más información, [vea Leer archivos con el Lector asincrónico o](reading-files-with-the-asynchronous-reader.md) Leer archivos con el Lector [sincrónico](reading-files-with-the-synchronous-reader.md).
4.  Antes de empezar a escribir, llame a [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) o [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) para cada salida y secuencia para las que se van a asignar búferes mediante el objeto reader. Para el lector sincrónico, llame a [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) o [**IWMSyncReader2::SetAllocateForStream en su**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) lugar.
5.  Comience a leer el archivo.

El objeto de lectura realizará llamadas a la devolución de llamada del asignador adecuado y recibirá ejemplos de la aplicación. La lógica de administración del búfer debe incluir una manera de indicar que un búfer puede usarse de nuevo. Normalmente, un búfer se vuelve a colocar en el grupo cuando se representa su contenido. En función de la aplicación, es posible que solo necesite algunos búferes en el grupo o muchos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




