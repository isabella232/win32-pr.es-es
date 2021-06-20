---
title: Compatibilidad con contenido del lado del dispositivo (PropertySheet)
description: Obtenga información sobre cómo usar la API de Shell de Windows o la API de WPD para obtener datos de objetos de dispositivo, a los que no se puede acceder a través del sistema de archivos en Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404198"
---
# <a name="supporting-device-side-content"></a>Compatibilidad con contenido del lado del dispositivo

Dado que el contenido del lado del dispositivo no es accesible a través del sistema de archivos en Windows Vista, deberá usar la API de Shell de Windows o la API de WPD para recuperar datos de objetos de dispositivo. Esta es la diferencia principal entre un controlador de hoja de propiedades normal y un controlador de hoja de propiedades WPD. El código de ejemplo siguiente muestra la recuperación de contenido del lado del dispositivo mediante la API de Windows Shell.

El primer paso es la inicialización de la lista de identificadores de elemento o PIDL. (Esta lista contiene el identificador único para el objeto de dispositivo especificado).


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



La función de inicialización llama a la función ExaminePIDLArray, que recupera las propiedades del objeto identificado por un \_ PIDL en la matriz PIDL.


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



Además de la inicialización y el procesamiento de la lista de identificadores de elemento, la aplicación deberá implementar el método IShellPropSheetExt::ReplacePage e insertar los controladores de reemplazo adecuados. El Shell de Windows llama a este método cada vez que está a punto de mostrar una hoja de propiedades reemplazable, lo que ofrece a la aplicación la oportunidad de invocar un controlador de reemplazo correspondiente. La palabra baja del primer parámetro para el método ReplacePage es un identificador de la hoja de propiedades determinada que Windows va a mostrar. Los valores pasados en la palabra baja del primer parámetro corresponden a los valores definidos en el archivo WpdShellExtension.h. Estos valores y sus descripciones aparecen en la tabla siguiente.



| Valor                                  | Descripción                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ DEVICE \_ GENERAL     | Corresponde a la pestaña general del dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ STORAGE \_ GENERAL    | Corresponde a la pestaña general de un objeto de almacenamiento que se encuentra en el dispositivo.    |
| WPDNSE \_ PROPSHEET \_ CONTENT \_ GENERAL    | Corresponde a la pestaña general del objeto de contenido que se encuentra en el dispositivo.      |
| REFERENCIAS DE CONTENIDO \_ DE PROPSHEET \_ DE WPDNSE \_ | Corresponde a la pestaña referencias de un objeto de contenido que se encuentra en el dispositivo. |
| RECURSOS DE CONTENIDO \_ DE PROPSHEET \_ DE WPDNSE \_  | Corresponde a la pestaña de recursos de un objeto de contenido que se encuentra en el dispositivo.  |
| DETALLES DEL CONTENIDO \_ DE LA HOJA DE PROPIEDADES \_ DE WPDNSE \_    | Corresponde a una pestaña de detalles de un objeto de contenido que se encuentra en el dispositivo.      |



 

En la extensión de hoja de propiedades de ejemplo, el método ReplacePage invoca dos controladores de reemplazo: \_ ReplaceDeviceGeneral y \_ ReplaceContentReferences. Estos controladores reemplazan el dispositivo general y las pestañas de referencias de contenido en las hojas de propiedades extensibles.


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



Dado que es posible que un usuario seleccione varios dispositivos, una aplicación deberá guardar la matriz PIDL devuelta por IShellExtInit::Initialize y, a continuación, examinar la palabra alta del primer parámetro en ReplacePage. Un valor de cero en esta palabra alta corresponde al primer elemento de la matriz PIDL, un valor de uno corresponde al segundo elemento, y así sucesivamente. En la función ReplacePage de la aplicación de ejemplo, este valor de palabra alta se pasa a ambos controladores de reemplazo. Estos controladores, a su vez, usan este valor para identificar un dispositivo determinado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



