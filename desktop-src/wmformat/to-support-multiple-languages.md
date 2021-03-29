---
title: Para la compatibilidad con varios idiomas
description: Para la compatibilidad con varios idiomas
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- SDK de Windows Media Format, compatible con varios idiomas
- SDK de Windows Media Format, compatibilidad con varios idiomas
- SDK de Windows Media Format, compatibilidad con idiomas
- Advanced Systems Format (ASF), compatible con varios idiomas
- ASF (formato de sistemas avanzados), compatible con varios idiomas
- Advanced Systems Format (ASF), compatibilidad con varios idiomas
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- Advanced Systems Format (ASF), compatibilidad con idiomas
- ASF (formato de sistemas avanzados), compatibilidad con idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995022"
---
# <a name="to-support-multiple-languages"></a>Para la compatibilidad con varios idiomas

Puede admitir varios lenguajes en streams y en metadatos. El núcleo de la compatibilidad con varios idiomas en el SDK de Windows Media Format es la interfaz [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , que mantiene una lista de los idiomas admitidos. La lista de idiomas proporciona a cada idioma compatible un índice, que se usa en varios objetos del SDK cuando se trabaja con varios idiomas.

El método [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) agrega un idioma a la lista. Puede identificar los idiomas que ya están en la lista obteniendo el número total de idiomas con [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) y, a continuación, recorrer en bucle los lenguajes que llaman a [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada uno. El índice de idioma está basado en cero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Para configurar la exclusión mutua por idioma

La configuración de un objeto de exclusión mutua simple por lenguaje es muy simple. Cada flujo está asociado ahora a un lenguaje. El lenguaje asociado a una secuencia se puede establecer mediante [**IWMStreamConfig3:: SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Una vez configurados todos los flujos mutuamente excluyentes, basta con crear un objeto de exclusión mutua como haría con cualquier otro tipo. A continuación, llame a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) pasando \_ \_ el lenguaje CLSID WMMUTEX para el tipo.

Las secuencias que se excluyen mutuamente por el lenguaje se vuelven más complicadas cuando las secuencias exclusivas también se excluyen mutuamente a través de la velocidad de bits. En este caso, debe realizar los siguientes pasos para usar registros mutuamente excluyentes:

1.  Cree un objeto de exclusión mutua para las secuencias de velocidades de bits diferentes en cada idioma. Para obtener más información sobre cómo crear un objeto de exclusión mutua por velocidad de bits, vea [usar la exclusión mutua de velocidad de bits múltiple](using-multiple-bit-rate-mutual-exclusion.md).
2.  Cree un objeto de exclusión mutua. Llame a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) y pase el \_ lenguaje CLSID WMMUTEX \_ para especificar la exclusividad por lenguaje.
3.  Obtenga un puntero a la interfaz [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) del objeto de exclusión mutua creado en el paso 2 llamando al método **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Llame al método [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una vez para cada lenguaje, para crear registros de secuencia que se excluyen mutuamente.
5.  Para cada registro creado en el paso 4, agregue las secuencias del lenguaje adecuado con llamadas a [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Para leer archivos con varios idiomas

El objeto de lector proporciona métodos para identificar los idiomas disponibles de las secuencias en un archivo. Puede recuperar el número de idiomas admitidos para una salida mediante una llamada a [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). A continuación, puede recuperar los detalles de cada idioma con llamadas a [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Puede especificar el idioma que se va a reproducir pasando el índice de ese idioma al lector con una llamada a [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Se seleccionará el idioma especificado al mismo tiempo que se mantiene la selección de secuencias automática para cualquier otro objeto de exclusión mutua del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**Interfaz IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Interfaz IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interfaz IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**Interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaz IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Interfaz IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




