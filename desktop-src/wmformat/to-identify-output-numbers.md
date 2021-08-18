---
title: Para identificar los números de salida
description: Para identificar los números de salida
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows SDK de formato multimedia, identificación de números de salida
- Formato de sistemas avanzados (ASF), identificación de números de salida
- ASF (formato de sistemas avanzados), identificación de números de salida
- Formato de sistemas avanzados (ASF), números de salida y formatos
- ASF (formato de sistemas avanzados), números de salida y formatos
- números y formatos de salida, identificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699385"
---
# <a name="to-identify-output-numbers"></a>Para identificar los números de salida

Para identificar los números de salida de un archivo cargado, realice los pasos siguientes. Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico. Cuando los nombres de interfaz varían, los métodos de lector sincrónicos se muestran entre paréntesis después de los métodos del lector asincrónico.

1.  Cree un objeto de lector y cargue un archivo para leerlo. Para obtener más información, vea Para crear un lector [y abrir un archivo](to-create-a-reader-and-open-a-file.md) (o Para crear un lector sincrónico y abrir un [archivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Recupere el número total de salidas del archivo llamando a [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader::GetOutputCount).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)
3.  Recorrer en bucle las salidas de una en una, realizando los pasos siguientes para cada una:
    -   Recupere la [**interfaz IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para la salida actual con una llamada a [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (o [**IWMSyncReader::GetOutputProps).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)
    -   Recupere la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la salida realizando dos llamadas a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Realice la primera llamada para obtener el tamaño de la estructura y, a continuación, asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada. Como alternativa, puede llamar a [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), que proporciona el tipo principal sin necesidad de asignar memoria para la estructura **WM MEDIA \_ \_ TYPE.** Puede omitir salidas del tipo principal incorrecto.
    -   Recupere el tipo de medio principal y el subtipo de medio de la **estructura WM \_ MEDIA \_ TYPE.** Estos valores se almacenan en los miembros de datos **majortype** y **subtype** respectivamente.
    -   Compruebe el valor de **WM \_ MEDIA \_ TYPE.formattype**. Especifica el tipo de estructura contenida en el búfer en **WM \_ MEDIA \_ TYPE.pbFormat**. Para obtener más información sobre los tipos de formato, vea [Tipos de medios](media-types.md).
    -   Asigne memoria para contener la estructura del tipo identificado en el paso anterior. Copie la estructura en la memoria asignada. Para audio y vídeo, esta estructura proporciona información esencial sobre cómo se deben representar los datos.

El lector sincrónico también proporciona métodos para recuperar asociaciones entre los números de salida y los números de secuencia. Para obtener más información, vea [Para buscar números de flujo y números de salida.](to-find-stream-numbers-and-output-numbers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**IWMMediaProps (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMOutputMediaProps (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




