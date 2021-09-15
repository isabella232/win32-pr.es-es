---
title: Para la compatibilidad con varios idiomas
description: Para la compatibilidad con varios idiomas
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows SDK de formato multimedia, compatible con varios idiomas
- Windows SDK de formato multimedia, compatibilidad con varios lenguajes
- Windows SDK de formato multimedia, compatibilidad con lenguajes
- Formato de sistemas avanzados (ASF), compatible con varios idiomas
- ASF (formato de sistemas avanzados), compatible con varios idiomas
- Formato de sistemas avanzados (ASF), compatibilidad con varios lenguajes
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- Formato de sistemas avanzados (ASF), compatibilidad con lenguajes
- ASF (formato de sistemas avanzados), compatibilidad con lenguajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247238"
---
# <a name="to-support-multiple-languages"></a>Para la compatibilidad con varios idiomas

Puede admitir varios lenguajes tanto en secuencias como en metadatos. El núcleo de la compatibilidad con varios lenguajes en el SDK Windows Media Format es la [**interfaz IWMLanguageList,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) que mantiene una lista de los idiomas admitidos. La lista de idiomas proporciona un índice a cada idioma admitido, que se usa en varios objetos del SDK al tratar con varios idiomas.

El [**método IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) agrega un lenguaje a la lista. Puede identificar los idiomas que ya están en la lista si obtiene el número total de idiomas con [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) y, a continuación, recorre en bucle los idiomas que llaman a [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada uno. El índice de lenguaje es de base cero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Para configurar la exclusión mutua por idioma

La configuración de un objeto de exclusión mutua simple por lenguaje es muy sencilla. Cada secuencia ahora está asociada a un idioma. El lenguaje asociado a una secuencia se puede establecer mediante [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Una vez configuradas todas las secuencias mutuamente excluyentes, simplemente cree un objeto de exclusión mutua como lo haría para cualquier otro tipo. A continuación, [**llame a IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) pasando CLSID \_ WMMUTEX \_ Language para el tipo.

Secuencias que se excluyen mutuamente por lenguaje se complican cuando las secuencias exclusivas también se excluyen mutuamente por velocidad de bits. En este caso, debe usar registros mutuamente excluyentes, realizando los pasos siguientes:

1.  Cree un objeto de exclusión mutua para las secuencias de velocidades de bits diferentes en cada idioma. Para obtener más información sobre cómo crear un objeto de exclusión mutua por velocidad de bits, vea [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).
2.  Cree un objeto de exclusión mutua. Llame [**a IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) y pase CLSID \_ WMMUTEX Language para especificar la \_ exclusión por idioma.
3.  Obtenga un puntero a la [**interfaz IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) del objeto de exclusión mutua creado en el paso 2 llamando al método **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Llame al [**método IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una vez para cada lenguaje para crear registros de flujo que se excluyen mutuamente.
5.  Para cada registro creado en el paso 4, agregue las secuencias del lenguaje adecuado con llamadas a [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Para leer archivos con varios idiomas

El objeto reader proporciona métodos para identificar los idiomas disponibles de las secuencias en un archivo. Puede recuperar el número de idiomas admitidos para una salida llamando a [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). A continuación, puede recuperar detalles sobre cada lenguaje con llamadas a [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Puede especificar el idioma que se va a reproducir pasando el índice de ese idioma al lector con una llamada a [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Esto seleccionará el idioma especificado mientras se mantiene la selección automática de secuencias para cualquier otro objeto de exclusión mutua del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**IWMLanguageList (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Interfaz IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interfaz IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**IWMReaderAdvanced2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMReaderAdvanced4 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Interfaz IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




