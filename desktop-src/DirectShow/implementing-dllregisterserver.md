---
description: Implementación de DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementación de DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152508"
---
# <a name="implementing-dllregisterserver"></a>Implementación de DllRegisterServer

El paso final consiste en implementar la función **DllRegisterServer** . El archivo DLL que contiene el componente debe exportar esta función. Una aplicación de instalación llamará a la función o cuando el usuario ejecute la herramienta Regsvr32.exe.

En el ejemplo siguiente se muestra una implementación mínima de **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



La función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea entradas del registro para cada componente de la


```
g_Templates
```



. Sin embargo, esta función tiene algunas limitaciones. En primer lugar, asigna todos los filtros a la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory), pero no todos los filtros pertenecen a esta categoría. Los filtros de captura y los filtros de compresión, por ejemplo, tienen sus propias categorías. En segundo lugar, si el filtro es compatible con un dispositivo de hardware, es posible que deba registrar dos partes adicionales de la información que **AMovieDLLRegisterServer2** no controla: la categoría *medio* y *PIN*. Un medio define un método de comunicación en un dispositivo de hardware, como un bus. La categoría PIN define la función de un PIN. Para obtener información sobre los medios, vea "KSPIN \_ Medium" en el kit de desarrollo de controladores (DDK) de Microsoft Windows. Para obtener una lista de las categorías de PIN, vea [conjunto de propiedades de PIN](pin-property-set.md).

Si desea especificar una categoría de filtro, un medio o una categoría de PIN, llame al método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) desde el interior de **DllRegisterServer**. Este método toma un puntero a una estructura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , que especifica información sobre el filtro.

Para complicar las cosas en cierto modo, la estructura **REGFILTER2** admite dos formatos diferentes para registrar los pin. El miembro **dwVersion** especifica el formato:

-   Si **dwVersion** es 1, el formato del PIN es **AMOVIESETUP \_ PIN** (descrito anteriormente).
-   Si **dwVersion** es 2, el formato del PIN es [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

La estructura **REGFILTERPINS2** incluye entradas para las categorías de anclaje medio y PIN. Además, utiliza marcas de bits para algunos elementos que **AMOVIESETUP \_ PIN** declara como valores booleanos.

En el ejemplo siguiente se muestra cómo llamar a **IFilterMapper2:: RegisterFilter** desde dentro de **DllRegisterServer**:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



