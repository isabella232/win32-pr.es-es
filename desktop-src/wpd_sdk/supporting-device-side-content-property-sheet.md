---
title: Compatibilidad del contenido del dispositivo (hoja)
description: Compatibilidad con contenido de Device-Side
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361082"
---
# <a name="supporting-device-side-content"></a>Compatibilidad con el contenido del dispositivo

Dado que el contenido del dispositivo no es accesible a través del sistema de archivos en Windows Vista, deberá usar la API de Shell de Windows o la API de WPD para recuperar los datos de los objetos de dispositivo. Esta es la diferencia principal entre un controlador de la hoja de propiedades normal y un controlador de la hoja de propiedades de WPD. En el código de ejemplo siguiente se muestra la recuperación del contenido del dispositivo mediante la API de Shell de Windows.

El primer paso es la inicialización de la lista de identificadores de elemento o PIDL. (Esta lista contiene el identificador único del objeto de dispositivo determinado).


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



La función de inicialización llama a la \_ función ExaminePIDLArray, que recupera las propiedades para el objeto identificado por un PIDL en la matriz PIDL.


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



Además de la inicialización y el procesamiento de la lista de identificadores de elemento, la aplicación deberá implementar el método IShellPropSheetExt:: ReplacePage e insertar los controladores de reemplazo adecuados. El shell de Windows llama a este método cada vez que está a punto de mostrar una hoja de propiedades reemplazable, lo que permite que la aplicación tenga la oportunidad de invocar un controlador de reemplazo correspondiente. La palabra baja del primer parámetro para el método ReplacePage es un identificador de la hoja de propiedades determinada que Windows está a punto de mostrar. Los valores pasados en la palabra baja del primer parámetro corresponden a los valores definidos en el archivo WpdShellExtension. h. Estos valores y sus descripciones aparecen en la tabla siguiente.



| Value                                  | Descripción                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ dispositivo \_ General     | Corresponde a la ficha General del dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ Storage \_ General    | Corresponde a la ficha General de un objeto de almacenamiento que se encuentra en el dispositivo.    |
| WPDNSE \_ \_ contenido \_ General de PROPSHEET    | Corresponde a la pestaña General del objeto de contenido que se encuentra en el dispositivo.      |
| referencias de contenido de WPDNSE \_ PROPSHEET \_ \_ | Corresponde a la pestaña referencias de un objeto de contenido que se encuentra en el dispositivo. |
| recursos de contenido de WPDNSE \_ PROPSHEET \_ \_  | Corresponde a la pestaña recursos de un objeto de contenido que se encuentra en el dispositivo.  |
| detalles de contenido de WPDNSE \_ PROPSHEET \_ \_    | Corresponde a una pestaña de detalles de un objeto de contenido que se encuentra en el dispositivo.      |



 

En la extensión de la hoja de propiedades de ejemplo, el método ReplacePage invoca dos controladores \_ de reemplazo: ReplaceDeviceGeneral y \_ ReplaceContentReferences. Estos controladores reemplazan las pestañas general Device y Content References en las hojas de propiedades extensibles.


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



Dado que es posible que un usuario seleccione varios dispositivos, una aplicación tendrá que guardar la matriz PIDL devuelta por IShellExtInit:: Initialize y, a continuación, examinar la palabra alta del primer parámetro en ReplacePage. Un valor de cero en esta palabra alta corresponde al primer elemento de la matriz PIDL, el valor uno corresponde al segundo elemento, etc. En la función ReplacePage de la aplicación de ejemplo, este valor de palabra alta se pasa a ambos controladores de reemplazo. Estos controladores, a su vez, usan este valor para identificar un dispositivo determinado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



