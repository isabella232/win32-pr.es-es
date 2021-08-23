---
description: Establecer propiedades de compresión de vídeo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Establecer propiedades de compresión de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583285"
---
# <a name="setting-video-compression-properties"></a>Establecer propiedades de compresión de vídeo

Los filtros de compresión de vídeo pueden admitir [**la interfaz IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) en sus pines de salida. Use esta interfaz para establecer propiedades de compresión, como la velocidad de fotogramas clave, el número de fotogramas predichos (P) por fotograma clave y la calidad de compresión relativa.

En primer lugar, llame al método [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para buscar el pin de salida del filtro y consulte el pin de la interfaz. Es posible que algunos filtros no admitan la interfaz en absoluto. Otros pueden exponer la interfaz, pero no admiten todas las propiedades de compresión. Para determinar qué propiedades se admiten, llame [**a IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Este método devuelve varios fragmentos de información:

-   Un conjunto de marcas de funcionalidades
-   Cadena descriptiva y cadena de número de versión
-   Valores predeterminados para la velocidad de fotogramas clave, la velocidad de fotogramas P y la calidad (cuando se admite)

El método tiene la sintaxis siguiente:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Los *parámetros pszVersion* y *pszDesc* son búferes de caracteres anchos que reciben la cadena de versión y la cadena de descripción. Los *parámetros cbVersion* y *cbDesc* reciben los tamaños de búfer necesarios en bytes (no caracteres). Los *parámetros lKeyFrame,* *lPFrame* y *dblQuality* reciben los valores predeterminados para la velocidad de fotogramas clave, la velocidad de fotogramas P y la calidad. La calidad se expresa como un número de punto flotante de 0,0 a 1,0. El *parámetro lCap* recibe un **OR** bit a bit de las marcas de funcionalidades, definidas por el tipo enumerado [**CompressionCaps.**](/windows/desktop/api/strmif/ne-strmif-compressioncaps)

Cualquiera de estos parámetros puede ser **NULL,** en cuyo caso el método omite ese parámetro. Por ejemplo, para asignar búferes para las cadenas de versión y descripción, primero llame al método **con NULL** en el primer y tercer parámetro. Use los valores devueltos para *cbVersion* y *cbDesc* para asignar los búferes y, a continuación, vuelva a llamar al método :


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



El valor de *lCap indica* cuál de los otros métodos **IAMVideoCompression** admite el filtro. Por ejemplo, si *lCap* contiene la marca CompressionCaps CanKeyFrame, puede llamar a \_ [**IAMVideoCompression::get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) para obtener la velocidad de fotogramas clave y [**IAMVideoCompression::p ut \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) para establecer la velocidad de fotogramas clave. Un valor negativo indica que el filtro usará el valor predeterminado, como se obtiene de [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Por ejemplo:


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



En el ejemplo de código siguiente se intenta encontrar la **interfaz IAMVideoCompression** en el pin de salida. Si se realiza correctamente, recupera los valores predeterminados y reales de las propiedades de compresión:


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Si usa la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para compilar el grafo, puede obtener la interfaz **IAMVideoCompression** llamando a [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), en lugar de usar **IBaseFilter::EnumPins**. El **método FindInterface** es un método auxiliar que busca filtros y marcadores en el gráfico para una interfaz especificada.

 

 

 



