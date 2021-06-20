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
# <a name="supporting-device-side-content"></a><span data-ttu-id="af511-103">Compatibilidad con contenido del lado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="af511-103">Supporting device-side content</span></span>

<span data-ttu-id="af511-104">Dado que el contenido del lado del dispositivo no es accesible a través del sistema de archivos en Windows Vista, deberá usar la API de Shell de Windows o la API de WPD para recuperar datos de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="af511-105">Esta es la diferencia principal entre un controlador de hoja de propiedades normal y un controlador de hoja de propiedades WPD.</span><span class="sxs-lookup"><span data-stu-id="af511-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="af511-106">El código de ejemplo siguiente muestra la recuperación de contenido del lado del dispositivo mediante la API de Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="af511-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="af511-107">El primer paso es la inicialización de la lista de identificadores de elemento o PIDL.</span><span class="sxs-lookup"><span data-stu-id="af511-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="af511-108">(Esta lista contiene el identificador único para el objeto de dispositivo especificado).</span><span class="sxs-lookup"><span data-stu-id="af511-108">(This list contains the unique identifier for the given device object.)</span></span>


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



<span data-ttu-id="af511-109">La función de inicialización llama a la función ExaminePIDLArray, que recupera las propiedades del objeto identificado por un \_ PIDL en la matriz PIDL.</span><span class="sxs-lookup"><span data-stu-id="af511-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


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



<span data-ttu-id="af511-110">Además de la inicialización y el procesamiento de la lista de identificadores de elemento, la aplicación deberá implementar el método IShellPropSheetExt::ReplacePage e insertar los controladores de reemplazo adecuados.</span><span class="sxs-lookup"><span data-stu-id="af511-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="af511-111">El Shell de Windows llama a este método cada vez que está a punto de mostrar una hoja de propiedades reemplazable, lo que ofrece a la aplicación la oportunidad de invocar un controlador de reemplazo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af511-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="af511-112">La palabra baja del primer parámetro para el método ReplacePage es un identificador de la hoja de propiedades determinada que Windows va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="af511-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="af511-113">Los valores pasados en la palabra baja del primer parámetro corresponden a los valores definidos en el archivo WpdShellExtension.h.</span><span class="sxs-lookup"><span data-stu-id="af511-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="af511-114">Estos valores y sus descripciones aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="af511-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="af511-115">Valor</span><span class="sxs-lookup"><span data-stu-id="af511-115">Value</span></span>                                  | <span data-ttu-id="af511-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="af511-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="af511-117">WPDNSE \_ PROPSHEET \_ DEVICE \_ GENERAL</span><span class="sxs-lookup"><span data-stu-id="af511-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="af511-118">Corresponde a la pestaña general del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="af511-119">WPDNSE \_ PROPSHEET \_ STORAGE \_ GENERAL</span><span class="sxs-lookup"><span data-stu-id="af511-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="af511-120">Corresponde a la pestaña general de un objeto de almacenamiento que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="af511-121">WPDNSE \_ PROPSHEET \_ CONTENT \_ GENERAL</span><span class="sxs-lookup"><span data-stu-id="af511-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="af511-122">Corresponde a la pestaña general del objeto de contenido que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="af511-123">REFERENCIAS DE CONTENIDO \_ DE PROPSHEET \_ DE WPDNSE \_</span><span class="sxs-lookup"><span data-stu-id="af511-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="af511-124">Corresponde a la pestaña referencias de un objeto de contenido que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="af511-125">RECURSOS DE CONTENIDO \_ DE PROPSHEET \_ DE WPDNSE \_</span><span class="sxs-lookup"><span data-stu-id="af511-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="af511-126">Corresponde a la pestaña de recursos de un objeto de contenido que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="af511-127">DETALLES DEL CONTENIDO \_ DE LA HOJA DE PROPIEDADES \_ DE WPDNSE \_</span><span class="sxs-lookup"><span data-stu-id="af511-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="af511-128">Corresponde a una pestaña de detalles de un objeto de contenido que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af511-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="af511-129">En la extensión de hoja de propiedades de ejemplo, el método ReplacePage invoca dos controladores de reemplazo: \_ ReplaceDeviceGeneral y \_ ReplaceContentReferences.</span><span class="sxs-lookup"><span data-stu-id="af511-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="af511-130">Estos controladores reemplazan el dispositivo general y las pestañas de referencias de contenido en las hojas de propiedades extensibles.</span><span class="sxs-lookup"><span data-stu-id="af511-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


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



<span data-ttu-id="af511-131">Dado que es posible que un usuario seleccione varios dispositivos, una aplicación deberá guardar la matriz PIDL devuelta por IShellExtInit::Initialize y, a continuación, examinar la palabra alta del primer parámetro en ReplacePage.</span><span class="sxs-lookup"><span data-stu-id="af511-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="af511-132">Un valor de cero en esta palabra alta corresponde al primer elemento de la matriz PIDL, un valor de uno corresponde al segundo elemento, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="af511-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="af511-133">En la función ReplacePage de la aplicación de ejemplo, este valor de palabra alta se pasa a ambos controladores de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="af511-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="af511-134">Estos controladores, a su vez, usan este valor para identificar un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="af511-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af511-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af511-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af511-136">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="af511-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



