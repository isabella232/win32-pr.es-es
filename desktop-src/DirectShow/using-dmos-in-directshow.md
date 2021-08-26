---
description: Uso de DDO en DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso de DDO en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078655"
---
# <a name="using-dmos-in-directshow"></a>Uso de DDO en DirectShow

Las aplicaciones basadas DirectShow pueden usar las DDO en un gráfico de filtros, a través [del filtro DMO contenedor.](dmo-wrapper-filter.md) Este filtro agrega un DMO controla todos los detalles del uso del DMO, como pasar datos a y desde el DMO, asignar objetos [**IMediaBuffer,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) etc.

Dado que el DMO agrega el filtro, la aplicación puede consultar el filtro para cualquier interfaz COM que el DMO expone. Sin embargo, la aplicación debe permitir que el filtro controle todas las operaciones de streaming en el DMO. Por ejemplo, no establezca tipos de medios, procese ningún búfer, vacíe el DMO, bloquee el DMO, habilite o deshabilite el control de calidad o establezca optimizaciones de vídeo.

Si conoce el identificador de clase (CLSID) de un DMO específico que desea usar, puede inicializar el filtro contenedor de DMO con ese DMO, como se muestra a continuación:

1.  Llame **a CoCreateInstance** para crear el filtro DMO wrapper.
2.  Consulte el filtro DMO wrapper para la [**interfaz IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)
3.  Llame al [**método IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) Especifique el CLSID de la DMO y el GUID de la DMO de la clase. Para obtener una lista de DMO, [vea DMO GUID.](dmo-guids.md)

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



La [**función DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera las DDO en el registro. Esta función usa un conjunto diferente de GUID de categoría de los que se usan para DirectShow filtros.

**Uso del enumerador de dispositivos del sistema con DDO**

En lugar de crear una DMO directamente, puede usar el enumerador de dispositivos del sistema [,](system-device-enumerator.md)que puede enumerar cualquier categoría DMO que sea compatible con el **método DMOEnum.** El enumerador de dispositivos del sistema también incluye DDO cuando enumera determinadas DirectShow de filtro. En la tabla siguiente se muestra la asignación entre DMO categorías y DirectShow categorías.



| Etiqueta | Valor |
|-----------------------------|--------------------------------|
| DMO Categoría                | DirectShow Equivalente          |
| CODIFICADOR DE AUDIO DMOCATEGORY \_ \_ | CLSID \_ AudioCompressorCategory |
| DESCODIFICADOR DE AUDIO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |
| CODIFICADOR DE VÍDEO DMOCATEGORY \_ \_ | CLSID \_ VideoCompressorCategory |
| DESCODIFICADOR DE VÍDEO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |



 

El enumerador de dispositivos del sistema devuelve una lista de objetos moniker. Si el moniker representa un DMO, el método **IMoniker::BindToObject** crea automáticamente el filtro contenedor DMO e inicializa con ese DMO. Por lo tanto, el hecho de que DMO esté implicado es transparente para la aplicación. Para obtener más información sobre el uso del enumerador de dispositivos del sistema, vea [Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

**Limitaciones**

Existen algunas limitaciones al usar DDO en DirectShow:

-   El DMO wrapper no admite DDO con cero entradas, varias entradas o cero salidas.
-   Todas las conexiones ancladas DMO filtro contenedor usan la [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   DirectShow Los servicios de edición no admiten DMO o transiciones basadas en la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DDO](using-dmos.md)
</dt> </dl>

 

 



