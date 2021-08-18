---
description: Elegir un filtro de compresión
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Elegir un filtro de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999225"
---
# <a name="choosing-a-compression-filter"></a>Elegir un filtro de compresión

Varios tipos de componentes de software pueden realizar la compresión de vídeo o audio, como:

-   Filtros DirectShow nativos
-   Códecs del Administrador de compresión de vídeo (VCM)
-   Códecs del Administrador de compresión de audio (ACM)
-   Objetos multimedia de DirectX (DDO)

En DirectShow, los códecs de VCM se encapsulan mediante el filtro de filtración de [AVI y](avi-compressor-filter.md)los códecs de ACM se encapsulan mediante el filtro contenedor [de ACM](acm-wrapper-filter.md). Las DDO se encapsulan mediante [el DMO contenedor de contenedores](dmo-wrapper-filter.md). El enumerador de dispositivos del sistema proporciona una manera coherente de enumerar y crear cualquiera de estos tipos de artefactos, sin preocuparse por el modelo subyacente.

Para obtener más información sobre el enumerador de dispositivos del sistema, [consulte Uso del enumerador de dispositivos del sistema.](using-the-system-device-enumerator.md) Brevemente, todos los DirectShow se clasifican por categoría y cada categoría se identifica mediante un GUID. En el caso de los vídeos, el GUID de categoría es CLSID \_ VideoCompressorCategory. Para los sonidos de audio, es CLSID \_ AudioCompressorCategory. Para enumerar una categoría determinada, el  enumerador de dispositivos del sistema crea un objeto enumerador que admite la [**interfaz IEnumMoniker.**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) La aplicación usa esta interfaz para recuperar monikers de dispositivo, donde cada moniker de dispositivo representa una instancia de un filtro DirectShow dispositivo. Puede usar el moniker para crear el filtro o para obtener el nombre descriptivo del dispositivo sin crear el filtro.

Para enumerar los vídeos o audios disponibles en el sistema del usuario, haga lo siguiente:

1.  Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el enumerador de dispositivos del sistema, que tiene un identificador de clase de CLSID \_ SystemDeviceEnum.
2.  Llame [**a ICreateDevEnum::CreateClassEnumerator con**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) el GUID de la categoría de filtro. El método devuelve un **puntero de interfaz IEnumMoniker.**
3.  Use el método IEnumMoniker::Next para enumerar los monikers del dispositivo. Este método devuelve una [**interfaz IMoniker,**](/windows/desktop/api/objidl/nn-objidl-imoniker) que representa el moniker.

Para obtener el nombre descriptivo de un moniker, haga lo siguiente:

1.  Llame al **método IMoniker::BindToStorage.** Este método devuelve un **puntero de interfaz IPropertyBag.**
2.  Use el **método IPropertyBag::Read** para leer la **propiedad FriendlyName.**

Normalmente, una aplicación mostraría una lista de reanados, para que el usuario pudiera elegir una. Por ejemplo, el código siguiente rellena un cuadro de lista con los nombres de los vídeos disponibles.


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



Para crear una instancia de filtro a partir del moniker, llame al **método IMoniker::BindToObject.** El método devuelve un [**puntero IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)


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



En el caso de los códecs VCM, cada moniker representa un códec determinado, aunque todos los códecs estén encapsulados por el mismo filtro de compresión AVI. Al **llamar a BindToObject** se crea una instancia de este filtro, inicializada para ese códec. Por este motivo, no puede llamar a **CoCreateInstance** directamente en el filtro compresión AVI. Debe pasar por el enumerador de dispositivos del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver acomprimir un archivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
