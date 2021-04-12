---
description: Elección de un filtro de compresión
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Elección de un filtro de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152666"
---
# <a name="choosing-a-compression-filter"></a>Elección de un filtro de compresión

Varios tipos de componentes de software pueden realizar compresión de audio o vídeo, como:

-   Filtros de DirectShow nativos
-   Códecs del administrador de compresión de vídeo (VCM)
-   Códecs del administrador de compresión de audio (ACM)
-   Objetos multimedia de DirectX (DMOs)

En DirectShow, los códecs VCM están incluidos en el [filtro del compresor AVI](avi-compressor-filter.md)y los códecs ACM se incluyen en el [filtro contenedor ACM](acm-wrapper-filter.md). Los DMOs se ajustan mediante el [filtro de contenedor de DMO](dmo-wrapper-filter.md). El enumerador de dispositivos del sistema proporciona una manera coherente de enumerar y crear cualquiera de estos tipos de compresores, sin preocuparse por el modelo subyacente.

Para obtener más información sobre el enumerador de dispositivos del sistema, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md). En Resumen, todos los filtros de DirectShow se clasifican por categoría y cada categoría se identifica mediante un GUID. En el caso de los compresores de vídeo, el GUID de categoría es CLSID \_ VideoCompressorCategory. En el caso de los compresores de audio, es CLSID \_ AudioCompressorCategory. Para enumerar una categoría determinada, el enumerador de dispositivos del sistema crea un objeto de *enumerador* que admite la interfaz [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) . La aplicación usa esta interfaz para recuperar monikers de dispositivo, donde cada moniker de dispositivo representa una instancia de un filtro de DirectShow. Puede utilizar el moniker para crear el filtro o para obtener el nombre descriptivo del dispositivo sin crear el filtro.

Para enumerar los compresores de audio o vídeo disponibles en el sistema del usuario, haga lo siguiente:

1.  Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el enumerador de dispositivos del sistema, que tiene un identificador de clase de CLSID \_ SystemDeviceEnum.
2.  Llame a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el GUID de la categoría de filtro. El método devuelve un puntero de interfaz **IEnumMoniker** .
3.  Use el método IEnumMoniker:: Next para enumerar los monikers de dispositivo. Este método devuelve una interfaz [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , que representa el moniker.

Para obtener el nombre descriptivo de un moniker, haga lo siguiente:

1.  Llame al método **IMoniker:: BindToStorage** . Este método devuelve un puntero a la interfaz **IPropertyBag** .
2.  Use el método **IPropertyBag:: Read** para leer la propiedad **FriendlyName** .

Normalmente, una aplicación mostraría una lista de compresores, de modo que el usuario pudiera elegir uno. Por ejemplo, el siguiente código rellena un cuadro de lista con los nombres de los compresores de vídeo disponibles.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Para crear una instancia de filtro a partir del moniker, llame al método **IMoniker:: BindToObject** . El método devuelve un puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



En el caso de los códecs VCM, cada moniker representa un códec determinado, aunque todos los códecs están encapsulados con el mismo filtro de compresión AVI. La llamada a **BindToObject** crea una instancia de este filtro, inicializada para ese códec. Por esta razón, no se puede llamar a **CoCreateInstance** directamente en el filtro de compresión AVI. Debe pasar por el enumerador de dispositivos del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver a comprimir un archivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
