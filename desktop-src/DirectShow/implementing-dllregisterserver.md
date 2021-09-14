---
description: Implementación de DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementación de DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161494"
---
# <a name="implementing-dllregisterserver"></a>Implementación de DllRegisterServer

El último paso es implementar la **función DllRegisterServer.** El archivo DLL que contiene el componente debe exportar esta función. Una aplicación de configuración llamará a la función o cuando el usuario ejecute Regsvr32.exe herramienta.

En el ejemplo siguiente se muestra una implementación mínima de **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



La [**función AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea entradas del Registro para cada componente de


```
g_Templates
```



. Sin embargo, esta función tiene algunas limitaciones. En primer lugar, asigna todos los filtros a la categoría "DirectShow Filters" (CLSID LegacyAmFilterCategory), pero no todos los filtros pertenecen \_ a esta categoría. Los filtros de captura y los filtros de compresión, por ejemplo, tienen sus propias categorías. En segundo lugar, si el filtro admite un dispositivo de hardware, es posible que tenga que  registrar dos fragmentos de información adicionales que **AMovieDLLRegisterServer2** no controla: el medio y la categoría *de pin*. Un medio define un método de comunicación en un dispositivo de hardware, como un bus. La categoría pin define la función de un pin. Para obtener información sobre los medios, consulte "KSPIN MEDIUM" en \_ Microsoft Windows Driver Development Kit (DDK). Para obtener una lista de categorías de pin, vea [Anclar conjunto de propiedades.](pin-property-set.md)

Si desea especificar una categoría de filtro, un medio o una categoría de pin, llame al método [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) desde **DllRegisterServer**. Este método toma un puntero a una [**estructura REGFILTER2,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que especifica información sobre el filtro.

Para complicar algo las cosas, la **estructura REGFILTER2** admite dos formatos diferentes para registrar los pines. El **miembro dwVersion** especifica el formato:

-   Si **dwVersion** es 1, el formato de pin es **el \_ PIN de AMOVIESETUP** (descrito anteriormente).
-   Si **dwVersion** es 2, el formato de pin es [**REGFILTERPINS2.**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2)

La **estructura REGFILTERPINS2** incluye entradas para las categorías de pin mediums y pin. Además, usa marcas de bits para algunos elementos que **el \_ PIN de AMOVIESETUP** declara como valores booleanos.

En el ejemplo siguiente se muestra cómo llamar a **IFilterMapper2::RegisterFilter** desde **DllRegisterServer**:


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



 

 



