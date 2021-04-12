---
title: Asignar búferes para la lectura de archivos
description: Asignar búferes para la lectura de archivos
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- SDK de Windows Media Format, leer archivos ASF
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
- Windows Media Format SDK, asignar búferes
- Advanced Systems Format (ASF), asignar búferes
- ASF (formato de sistemas avanzados), asignar búferes
- Advanced Systems Format (ASF), asignación de búfer
- ASF (formato de sistemas avanzados), asignación de búfer
- asignación de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420225"
---
# <a name="allocating-buffers-for-file-reading"></a>Asignar búferes para la lectura de archivos

En el escenario de lectura de archivos más básico, los búferes que se usan para proporcionar ejemplos se asignan mediante el objeto de lectura (el objeto lector o el objeto lector sincrónico). Sin embargo, puede asignar búferes personalmente. Para obtener más información sobre las ventajas de la asignación de sus propios búferes, consulte [compatibilidad con el ejemplo](user-allocated-sample-support.md)de asignación de usuarios.

Para usar sus propios búferes para la lectura de archivos, realice los pasos siguientes.

1.  Implemente una devolución de llamada o devoluciones de llamada para que el lector llame cuando necesite un búfer. Si está leyendo ejemplos de salida, use [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Si está leyendo ejemplos de secuencias, use [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Incluya la lógica para administrar los búferes que mejor se adapte a su aplicación.
2.  Asigne un grupo de búferes que usará para la lectura de archivos.
    -   Busque el tamaño necesario para los búferes mediante una llamada a [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) o [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) para cada salida o secuencia para la que se usa el búfer. Si usa el lector sincrónico, use [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) o [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) en su lugar.
    -   Cree cada búfer para el grupo.
3.  Configure el lector o el lector sincrónico para lectura. Para obtener más información, vea [leer archivos con el lector asincrónico](reading-files-with-the-asynchronous-reader.md) o [leer archivos con el lector sincrónico](reading-files-with-the-synchronous-reader.md).
4.  Antes de empezar a escribir, llame a [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) o [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) para cada salida y flujo para los que va a asignar búferes mediante el objeto de lector. En el caso del lector sincrónico, llame a [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) o [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) en su lugar.
5.  Empiece a leer el archivo.

El objeto de lectura realizará las llamadas a la devolución de llamada de asignador adecuada y obtendrá ejemplos de la aplicación. La lógica de administración de búfer debe incluir una manera de indicar que un búfer puede volver a usarse. Normalmente, un búfer se vuelve a colocar en el grupo cuando se representa su contenido. Dependiendo de la aplicación, es posible que necesite unos pocos búferes en el grupo o muchos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




