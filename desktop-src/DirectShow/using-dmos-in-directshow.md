---
description: Uso de DDO en DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso de DDO en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908693"
---
# <a name="using-dmos-in-directshow"></a>Uso de DDO en DirectShow

Las aplicaciones basadas en DirectShow pueden usar DDO en un gráfico de filtros, a través del filtro [contenedor de DMO.](dmo-wrapper-filter.md) Este filtro agrega un DMO y controla todos los detalles del uso de DMO, como pasar datos a y desde el DMO, asignar objetos [**IMediaBuffer,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) etc.

Dado que el filtro agrega el DMO, la aplicación puede consultar el filtro para cualquier interfaz COM que exponga el DMO. Sin embargo, la aplicación debe permitir que el filtro controle todas las operaciones de streaming en el DMO. Por ejemplo, no establezca tipos de medios, procese ningún búfer, vacíe el DMO, bloquee el DMO, habilite o deshabilite el control de calidad o establezca optimizaciones de vídeo.

Si conoce el identificador de clase (CLSID) de un DMO específico que desea usar, puede inicializar el filtro contenedor de DMO con ese DMO, como se muestra a continuación:

1.  Llame **a CoCreateInstance** para crear el filtro contenedor de DMO.
2.  Consulte el filtro contenedor de DMO para la [**interfaz IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)
3.  Llame al [**método IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) Especifique el CLSID del DMO y el GUID de la categoría de DMO. Para obtener una lista de categorías de DMO, vea [GUID de DMO](dmo-guids.md).

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



La [**función DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera las DDO en el Registro. Esta función usa un conjunto diferente de GUID de categoría de los usados para los filtros de DirectShow.

**Uso del enumerador de dispositivos del sistema con DDO**

En lugar de crear un DMO directamente, puede usar el enumerador de dispositivos del sistema [,](system-device-enumerator.md)que puede enumerar cualquier categoría de DMO que sea compatible con el **método DMOEnum.** El enumerador de dispositivos del sistema también incluye DDO cuando enumera determinadas categorías de filtro de DirectShow. En la tabla siguiente se muestra la asignación entre las categorías DMO y DirectShow.



| Etiqueta | Value |
|-----------------------------|--------------------------------|
| Categoría DMO                | Equivalente de DirectShow          |
| CODIFICADOR DE AUDIO DMOCATEGORY \_ \_ | CLSID \_ AudioCompressorCategory |
| DESCODIFICADOR DE AUDIO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |
| CODIFICADOR DE VÍDEO DMOCATEGORY \_ \_ | CLSID \_ VideoCompressorCategory |
| DESCODIFICADOR DE VÍDEO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |



 

El enumerador de dispositivos del sistema devuelve una lista de objetos moniker. Si el moniker representa un DMO, el método **IMoniker::BindToObject** crea automáticamente el filtro contenedor DMO y lo inicializa con ese DMO. Por lo tanto, el hecho de que un DMO esté implicado es transparente para la aplicación. Para obtener más información sobre el uso del enumerador de dispositivos del sistema, vea [Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

**Limitaciones**

Existen algunas limitaciones al usar las DDO en DirectShow:

-   El filtro contenedor DMO no admite DDO con cero entradas, varias entradas o cero salidas.
-   Todas las conexiones ancladas en el filtro contenedor de DMO usan [**la interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   DirectShow Editing Services no admite transiciones ni efectos basados en DMO.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DDO](using-dmos.md)
</dt> </dl>

 

 



