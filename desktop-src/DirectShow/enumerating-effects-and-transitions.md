---
description: Enumerar efectos y transiciones
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Enumerar efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677107"
---
# <a name="enumerating-effects-and-transitions"></a>Enumerar efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

DirectShow proporciona un objeto de [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar los dispositivos. Puede usarlo para recuperar monikers para efectos o transiciones instalados en el sistema del usuario.

El enumerador de dispositivos del sistema expone la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) . Devuelve los enumeradores de categoría para las categorías de dispositivos especificadas. Un enumerador de categoría, a su vez, expone la interfaz [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) y devuelve monikers para cada dispositivo de la categoría. Para obtener una explicación detallada del uso de **ICreateDevEnum**, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md). A continuación se encuentra un breve resumen, específico de los servicios de edición de DirectShow.

Para enumerar los efectos o las transiciones, realice los pasos siguientes.

1.  Cree una instancia del enumerador de dispositivos del sistema.
2.  Llame al método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) para recuperar un enumerador de categoría. Las categorías se definen por los identificadores de clase (CLSID). Use CLSID \_ VideoEffects1Category para los efectos o CLSID \_ VideoEffects2Category para las transiciones.
3.  Llame a **IEnumMoniker:: Next** para recuperar cada moniker de la enumeración.
4.  Para cada moniker, llame a **IMoniker:: BindToStorage** para recuperar el contenedor de propiedades asociado.

La bolsa de propiedades contiene el nombre descriptivo y el identificador único global (GUID) para el efecto o la transición. Una aplicación puede mostrar una lista de nombres descriptivos y, a continuación, obtener el GUID correspondiente.

En el ejemplo de código siguiente se muestran estos pasos.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
