---
title: Asignar formatos de salida
description: Asignar formatos de salida
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- SDK de Windows Media Format, asignar formatos de salida
- Advanced Systems Format (ASF), asignar formatos de salida
- ASF (formato de sistemas avanzados), asignar formatos de salida
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, asignar
- códecs, números de salida y formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105656315"
---
# <a name="assigning-output-formats"></a>Asignar formatos de salida

Algunos códecs pueden descomprimir los datos multimedia digitales en varios formatos sin comprimir. Puede buscar todos los formatos admitidos para una salida específica mediante el lector asincrónico o el lector sincrónico.

Para examinar todos los formatos disponibles para una salida, realice los pasos siguientes. Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico. Si los nombres de interfaz varían, los métodos de lectura sincrónicos se enumeran entre paréntesis después de los métodos del lector asincrónico.

1.  Cree un objeto lector y cargue un archivo para leerlo. Para obtener más información, vea [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md) (o [para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Determine la salida para la que desea buscar los formatos disponibles. Si aún no sabe qué salida desea usar, puede identificar las salidas en el archivo mediante los procedimientos de [para identificar los números de salida](to-identify-output-numbers.md).
3.  Recupere el número total de formatos disponibles para la salida deseada llamando a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Recorra los formatos disponibles de uno en uno, realizando los pasos siguientes para cada uno:
    -   Recupere la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para el formato de salida actual llamando a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (o [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).
    -   Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de salida realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Realice la primera llamada para obtener el tamaño de la estructura, después asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada.
    -   Busque el subtipo de medio del formato de salida en **tipo de medio de WM \_ \_ . subtipo**.
    -   En el caso de vídeo, si el subtipo actual es el formato que desea usar para la salida, salga del bucle. De lo contrario, vaya a la siguiente iteración.

        En el caso de audio, debe comprobar los valores de la estructura **WAVEFORMATEX** en función de sus requisitos. **WM \_ MEDIA \_ Type. pbFormat** apunta a la estructura **WAVEFORMATEX** para las salidas de audio.

5.  Cuando haya encontrado el resultado deseado, establézcalo para usarlo con el lector mediante una llamada a [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). Debe pasar un puntero a la interfaz **IWMOutputMediaProps** obtenida en el primer paso del bucle.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interfaz IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




