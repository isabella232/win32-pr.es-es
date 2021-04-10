---
description: Usar DMOs en DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Usar DMOs en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156732"
---
# <a name="using-dmos-in-directshow"></a>Usar DMOs en DirectShow

Las aplicaciones basadas en DirectShow pueden usar DMOs en un gráfico de filtros, a través del filtro de [contenedor de DMO](dmo-wrapper-filter.md) . Este filtro agrega un DMO y controla todos los detalles del uso de DMO, como pasar datos hacia y desde DMO, asignando objetos [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) , etc.

Como el filtro agrega DMO, la aplicación puede consultar el filtro para las interfaces COM que expone el DMO. Sin embargo, la aplicación debe permitir que el filtro controle todas las operaciones de streaming en DMO. Por ejemplo, no establezca tipos de medios, procese ningún búfer, vacíe el DMO, bloquee el DMO, habilite o deshabilite el control de calidad o establezca optimizaciones de vídeo.

Si conoce el identificador de clase (CLSID) de un DMO específico que desea usar, puede inicializar el filtro de contenedor de DMO con ese DMO, como se indica a continuación:

1.  Llame a **CoCreateInstance** para crear el filtro de contenedor de DMO.
2.  Consulte el filtro de contenedor de DMO para la interfaz [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Llame al método [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . Especifique el CLSID de DMO y el GUID de la categoría de DMO. Para obtener una lista de las categorías de DMO, consulte los [GUID de DMO](dmo-guids.md).

El siguiente código muestra estos pasos:


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



La función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOs en el registro. Esta función utiliza un conjunto diferente de GUID de categoría de los que se usan para los filtros de DirectShow.

**Usar el enumerador de dispositivos del sistema con DMOs**

En lugar de crear directamente un DMO, puede usar el [enumerador de dispositivos del sistema](system-device-enumerator.md), que puede enumerar cualquier categoría de DMO compatible con el método **DMOEnum** . El enumerador de dispositivos del sistema también incluye DMOs cuando enumera determinadas categorías de filtros de DirectShow. En la tabla siguiente se muestra la asignación entre categorías de DMO y categorías de DirectShow.



|                             |                                |
|-----------------------------|--------------------------------|
| Categoría de DMO                | Equivalente de DirectShow          |
| \_codificador de audio DMOCATEGORY \_ | CLSID \_ AudioCompressorCategory |
| descodificador de audio de DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |
| \_codificador de vídeo de DMOCATEGORY \_ | CLSID \_ VideoCompressorCategory |
| descodificador de vídeo de DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |



 

El enumerador de dispositivos del sistema devuelve una lista de objetos moniker. Si el moniker representa un DMO, el método **IMoniker:: BindToObject** crea automáticamente el filtro de contenedor de DMO y lo inicializa con dicho DMO. Por lo tanto, el hecho de que un DMO esté implicado es transparente para la aplicación. Para obtener más información acerca del uso del enumerador de dispositivos del sistema, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

**Limitaciones**

Hay algunas limitaciones al usar DMOs en DirectShow:

-   El filtro de contenedor de DMO no admite DMOs con cero entradas, entradas múltiples o salidas cero.
-   Todas las conexiones de PIN en el filtro de contenedor de DMO usan la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Los servicios de edición de DirectShow no admiten efectos ni transiciones basados en DMO.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DMOs](using-dmos.md)
</dt> </dl>

 

 



