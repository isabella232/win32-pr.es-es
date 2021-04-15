---
title: Para identificar los números de salida
description: Para identificar los números de salida
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- SDK de Windows Media Format, identificar números de salida
- Advanced Systems Format (ASF), identificar números de salida
- ASF (formato de sistemas avanzados), identificar números de salida
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, identificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714327"
---
# <a name="to-identify-output-numbers"></a>Para identificar los números de salida

Para identificar los números de salida de un archivo cargado, realice los pasos siguientes. Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico. Si los nombres de interfaz varían, los métodos de lectura sincrónicos se enumeran entre paréntesis después de los métodos del lector asincrónico.

1.  Cree un objeto lector y cargue un archivo para leerlo. Para obtener más información, vea [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md) (o [para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Recupere el número total de salidas del archivo mediante una llamada a [**IWMReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Recorra las salidas de una en una, siguiendo estos pasos para cada una de ellas:
    -   Recupere la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para la salida actual con una llamada a [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (o [**IWMSyncReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).
    -   Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la salida realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Realice la primera llamada para obtener el tamaño de la estructura, después asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada. Como alternativa, puede llamar a [**IWMMediaProps:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), que ofrece el tipo principal sin necesidad de asignar memoria para la estructura de **\_ \_ tipo de medio de WM** . Puede omitir las salidas del tipo principal incorrecto.
    -   Recupere el tipo de medio principal y el subtipo de medio de la estructura de **\_ \_ tipo de medio de WM** . Estos valores se almacenan en miembros de datos **majortype** y **SubType** respectivamente.
    -   Compruebe el valor de **tipo de medio de WM \_ \_ . FormatType**. Especifica el tipo de estructura que contiene el búfer en el **tipo de medio de WM \_ \_ . pbFormat**. Para obtener más información sobre los tipos de formato, consulte [tipos de medios](media-types.md).
    -   Asigne memoria para que contenga la estructura del tipo identificado en el paso anterior. Copie la estructura en la memoria asignada. En audio y vídeo, esta estructura proporciona información esencial sobre cómo se deben representar los datos.

El lector sincrónico también proporciona métodos para recuperar las asociaciones entre los números de salida y los números de flujo. Para obtener más información, vea [para buscar números de secuencia y números de salida](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

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

 

 




