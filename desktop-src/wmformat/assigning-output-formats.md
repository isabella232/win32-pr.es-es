---
title: Asignar formatos de salida
description: Asignar formatos de salida
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows SDK de formato multimedia, asignación de formatos de salida
- Formato de sistemas avanzados (ASF), asignación de formatos de salida
- ASF (formato de sistemas avanzados), asignación de formatos de salida
- Formato de sistemas avanzados (ASF), números de salida y formatos
- ASF (formato de sistemas avanzados), números de salida y formatos
- números y formatos de salida, asignación
- códecs, números de salida y formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80672419a032b2fff779259ffc6dcebfbe9e9a569f9d4b7afbb75ae5a84fac2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659379"
---
# <a name="assigning-output-formats"></a>Asignar formatos de salida

Algunos códecs pueden descomprimir datos multimedia digitales en varios formatos sin comprimir. Puede encontrar todos los formatos admitidos para una salida específica mediante el lector asincrónico o el lector sincrónico.

Para examinar todos los formatos disponibles para una salida, realice los pasos siguientes. Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico. Cuando los nombres de interfaz varían, los métodos de lector sincrónicos se muestran entre paréntesis después de los métodos del lector asincrónico.

1.  Cree un objeto de lector y cargue un archivo para leerlo. Para obtener más información, vea [Para crear un](to-create-a-reader-and-open-a-file.md) lector y abrir un archivo (o Para crear un lector [sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Determine la salida para la que desea encontrar los formatos disponibles. Si aún no sabe qué salida desea usar, puede identificar las salidas en el archivo mediante los procedimientos de Para identificar números [de salida](to-identify-output-numbers.md).
3.  Recupere el número total de formatos disponibles para la salida deseada llamando a [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader::GetOutputFormatCount).**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)
4.  Recorrer en bucle los formatos disponibles de uno en uno, realizando los pasos siguientes para cada uno:
    -   Recupere la [**interfaz IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para el formato de salida actual llamando a [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (o [**IWMSyncReader::GetOutputFormat).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)
    -   Recupere la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de salida realizando dos llamadas a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Realice la primera llamada para obtener el tamaño de la estructura y, a continuación, asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada.
    -   Busque el subtipo de medios del formato de salida en **WM \_ MEDIA \_ TYPE.subtype**.
    -   En el caso del vídeo, si el subtipo actual es el formato que desea usar para la salida, salga del bucle. De lo contrario, vaya a la siguiente iteración.

        En el caso del audio, debe comprobar los valores de la estructura **DESATEX con** sus requisitos. **WM \_ MEDIA \_ TYPE.pbFormat** apunta a la estructura **DE FORMA DEFORMESATEX** para las salidas de audio.

5.  Cuando haya encontrado el resultado deseado, estadúelo para usarlo con el lector mediante una llamada a [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader::SetOutputProps).**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops) Debe pasar un puntero a la **interfaz IWMOutputMediaProps** obtenida en el primer paso del bucle.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMMediaProps (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMOutputMediaProps (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




