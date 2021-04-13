---
description: Usar el enumerador de dispositivos del sistema
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Usar el enumerador de dispositivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568640"
---
# <a name="using-the-system-device-enumerator"></a>Usar el enumerador de dispositivos del sistema

El enumerador de dispositivos del sistema proporciona una manera uniforme de enumerar, por categoría, los filtros registrados en el sistema de un usuario. Además, distingue entre dispositivos de hardware individuales, aunque el mismo filtro los admita. Esto es especialmente útil para los dispositivos que usan el Modelo de controlador de Windows (WDM) y el filtro KSProxy. Por ejemplo, el usuario puede tener varios dispositivos de captura de vídeo WDM, todos compatibles con el mismo filtro. El enumerador de dispositivos del sistema los trata como instancias de dispositivo independientes.

El enumerador de dispositivos del sistema funciona mediante la creación de un enumerador para una categoría específica, como la captura de audio o la compresión de vídeo. El enumerador de categoría devuelve un moniker único para cada dispositivo de la categoría. El enumerador de categoría incluye automáticamente los dispositivos Plug and Play relevantes de la categoría. Para obtener una lista de categorías, vea [filtrar categorías](filter-categories.md).

Para usar el enumerador de dispositivos del sistema, haga lo siguiente:

1.  Cree el enumerador de dispositivos del sistema llamando a **CoCreateInstance**. El identificador de clase (CLSID) es CLSID \_ SystemDeviceEnum.
2.  Obtenga un enumerador de categoría mediante una llamada a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el CLSID de la categoría deseada. Este método devuelve un puntero de interfaz **IEnumMoniker** . Si la categoría está vacía (o no existe), el método devuelve S \_ false en lugar de un código de error. Si es así, el puntero de **IEnumMoniker** devuelto es **null** y al desreferenciarlo se producirá una excepción. Por lo tanto, pruebe explícitamente \_ si es correcto cuando llame a **CreateClassEnumerator**, en lugar de llamar a la macro con **éxito** habitual.
3.  Use el método **IEnumMoniker:: Next** para enumerar cada moniker. Este método devuelve un puntero de interfaz **IMoniker** . Cuando el método **siguiente** alcanza el final de la enumeración, también devuelve s \_ false, de modo que se comprueba de nuevo si hay un valor \_ correcto.
4.  Para recuperar el nombre descriptivo del dispositivo (por ejemplo, para mostrarlo en la interfaz de usuario), llame al método **IMoniker:: BindToStorage** .
5.  Para crear e inicializar el filtro de DirectShow que administra el dispositivo, llame a **IMoniker:: BindToObject** en el moniker. Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico.

En el siguiente diagrama se muestra este proceso.

![enumerar dispositivos](images/sysdevenum.png)

En el ejemplo siguiente se muestra cómo enumerar los compresores de vídeo instalados en el sistema del usuario. Por motivos de brevedad, en el ejemplo se realiza una comprobación de errores mínima.


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**Monikers de dispositivo**

En el caso de los monikers de dispositivo, puede pasar el moniker al método [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) para crear un filtro de captura para el dispositivo. Para ver el código de ejemplo, consulte la documentación de ese método.

El método **IMoniker:: getDisplayName** devuelve el nombre para mostrar del moniker. Aunque el nombre para mostrar se puede leer, normalmente no se muestra a un usuario final. En su lugar, obtenga el nombre descriptivo del contenedor de propiedades, como se ha descrito anteriormente.

El método **IMoniker::P arsedisplayname** o la función **MkParseDisplayName** se pueden usar para crear un moniker de dispositivo predeterminado para una categoría de filtro determinada. Use un nombre para mostrar con el formato `@device:*:{category-clsid}` , donde `category-clsid` es la representación de cadena del GUID de categoría. El moniker predeterminado es el primer moniker devuelto por el enumerador de dispositivos de esa categoría.

 

 



