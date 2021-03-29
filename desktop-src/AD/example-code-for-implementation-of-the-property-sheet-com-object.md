---
title: Código de ejemplo para la implementación del objeto COM de la hoja de propiedades
description: El siguiente ejemplo de código se puede usar para implementar una Active Directory extensión de la hoja de propiedades.
ms.assetid: aeee870e-1a0e-437f-a724-0bbac30f5e34
ms.tgt_platform: multiple
keywords:
- Código de ejemplo para la implementación de la hoja de propiedades objeto COM AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ea28b3c1de9fa69d14db3168db821d8b38cfc5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487443"
---
# <a name="example-code-for-implementation-of-the-property-sheet-com-object"></a><span data-ttu-id="7a075-104">Código de ejemplo para la implementación del objeto COM de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="7a075-104">Example Code for Implementation of the Property Sheet COM Object</span></span>

<span data-ttu-id="7a075-105">El siguiente ejemplo de código se puede usar para implementar una Active Directory extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a075-105">The following code example can be used to implement an Active Directory property sheet extension.</span></span>

## <a name="ishellextinit-implementation"></a><span data-ttu-id="7a075-106">Implementación de IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="7a075-106">IShellExtInit Implementation</span></span>

<span data-ttu-id="7a075-107">El siguiente ejemplo de código de C++ se puede usar para implementar los métodos [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .</span><span class="sxs-lookup"><span data-stu-id="7a075-107">The following C++ code example can be used to implement the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) methods.</span></span>


```C++
/**************************************************************************

    CPropSheetExt::Initialize()

**************************************************************************/

STDMETHODIMP CPropSheetExt::Initialize( LPCITEMIDLIST pidlFolder,
                                        IDataObject *pDataObj,
                                        HKEY hKeyProgId)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr = S_OK;

    if(NULL == pDataObj)
    {
        return E_INVALIDARG;
    }

    hr = pDataObj->QueryInterface(IID_IDataObject, (LPVOID*)&m_pdo);
    if(FAILED(hr))
    {
        return hr;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = m_pdo->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            LPWSTR  pwszName = (LPWSTR)((LPBYTE)pdson + pdson->aObjects[0].offsetName);
            
            m_pwszADsPath = (LPWSTR)GlobalAlloc(GPTR, (lstrlenW(pwszName) + 1) * sizeof(WCHAR));
            if(m_pwszADsPath)
            {
                wcscpy_s(m_pwszADsPath, pwszName);
            }
            
            LPWSTR  pwszClass = (LPWSTR)((LPBYTE)pdson + pdson->aObjects[0].offsetClass);
            pwszClass = NULL;

            GlobalUnlock(stm.hGlobal);
        }
        
        ReleaseStgMedium(&stm);
    }

    m_hwndNotifyObj = CreateADsNotificationObject(pDataObj);

    if(m_hwndNotifyObj)
    {
        ADSPROPINITPARAMS   InitParams;
        
        hr = GetADsPageInfo(m_hwndNotifyObj, &InitParams);
        if(SUCCEEDED(hr))
        {
            if(InitParams.pDsObj)
            {
                hr = InitParams.pDsObj->QueryInterface( IID_IDirectoryObject, 
                                                        (LPVOID*) & m_pDirObj);
            }
        }
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DS_DISPLAY_SPEC_OPTIONS);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        PDSDISPLAYSPECOPTIONS   pdso;
        
        pdso = (PDSDISPLAYSPECOPTIONS)GlobalLock(stm.hGlobal);
        if(pdso)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pDispSpecOpts = (PDSDISPLAYSPECOPTIONS)GlobalAlloc(GPTR, dwBytes);
            if(m_pDispSpecOpts)
            {
                CopyMemory(m_pDispSpecOpts, pdso, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }

        ReleaseStgMedium(&stm);
    }

    return hr;
}

```



## <a name="ishellpropsheetext-implementation"></a><span data-ttu-id="7a075-108">Implementación de IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="7a075-108">IShellPropSheetExt Implementation</span></span>

<span data-ttu-id="7a075-109">El siguiente ejemplo de código de C++ se puede usar para implementar los métodos [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="7a075-109">The following C++ code example can be used to implement the [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) methods.</span></span>


```C++
/**************************************************************************

    CPropSheetExt::AddPages()

**************************************************************************/

STDMETHODIMP CPropSheetExt::AddPages(   LPFNADDPROPSHEETPAGE pfnAddPage, 
                                        LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = g_szPageTitle;
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = NULL;
    psp.pfnCallback   = PageCallbackProc;
    //pass the object pointer to the dialog box
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
                
    if(hPage) 
    {
        if(pfnAddPage(hPage, lParam))
        {
            /*
            Maintain this object until the page is released in 
            PageCallbackProc.
            */
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }

    return E_FAIL;
}

/**************************************************************************

    CPropSheetExt::ReplacePage()

**************************************************************************/

STDMETHODIMP CPropSheetExt::ReplacePage(    UINT uPageID, 
                                            LPFNADDPROPSHEETPAGE lpfnAddPage, 
                                            LPARAM lParam)
{
    return E_NOTIMPL;
}

```



## <a name="miscellaneous-implementation"></a><span data-ttu-id="7a075-110">Implementación de varios</span><span class="sxs-lookup"><span data-stu-id="7a075-110">Miscellaneous Implementation</span></span>

<span data-ttu-id="7a075-111">El siguiente ejemplo de código de C++ se puede usar para implementar los métodos de utilidad y las funciones que se usan en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="7a075-111">The following C++ code example can be used to implement the utility methods and functions used in the previous code example.</span></span>


```C++
HWND CreateADsNotificationObject(IDataObject *pDataObject)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;
    HWND        hwndNotifyObject = NULL;

    /*
    The "DsAdminMultiSelectClipFormat" clipboard format is supported by the 
    data object if the Active Directory Users and Computers snap-in supports 
    multi-selection property sheets.
    */
    fe.cfFormat = RegisterClipboardFormat(TEXT("DsAdminMultiSelectClipFormat"));
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObject->GetData(&fe, &stm);
    if (SUCCEEDED(hr))
    {
        PWSTR pwzUniqueID = (LPWSTR)GlobalLock(stm.hGlobal);

        if (pwzUniqueID)
        {
            hr = ADsPropCreateNotifyObj(pDataObject, pwzUniqueID, &hwndNotifyObject);

            GlobalUnlock(stm.hGlobal);
        }
            
        ReleaseStgMedium(&stm);
    }
    else
    {
        fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
        fe.ptd = NULL;
        fe.dwAspect = DVASPECT_CONTENT;
        fe.lindex = -1;
        fe.tymed = TYMED_HGLOBAL;
        hr = pDataObject->GetData(&fe, &stm);
        if(SUCCEEDED(hr))
        {
            LPDSOBJECTNAMES pdson = (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

            if(pdson)
            {
                LPWSTR  pwszName = (LPWSTR)((LPBYTE)pdson + pdson->aObjects[0].offsetName);
                
                hr = ADsPropCreateNotifyObj(pDataObject, pwszName, &hwndNotifyObject);

                GlobalUnlock(stm.hGlobal);
            }
            
            ReleaseStgMedium(&stm);
        }
    }

    return hwndNotifyObject;
}

/**************************************************************************

    GetADsPageInfo()
   
**************************************************************************/

HRESULT GetADsPageInfo(HWND hwndNotifyObject, ADSPROPINITPARAMS *pip)
{
    if(!IsWindow(hwndNotifyObject))
    {
        return E_INVALIDARG;
    }

    ADSPROPINITPARAMS   InitParams;
    
    InitParams.dwSize = sizeof(ADSPROPINITPARAMS);
    if(ADsPropGetInitInfo(hwndNotifyObject, &InitParams))
    {
        *pip = InitParams;
    
        return InitParams.hr;
    }
    
    return E_FAIL;
}

/**************************************************************************

    CPropSheetExt::PageDlgProc

**************************************************************************/

#define THIS_POINTER_PROP  TEXT("ThisPointerProperty")

BOOL CALLBACK CPropSheetExt::PageDlgProc(   HWND hWnd, 
                                            UINT uMsg, 
                                            WPARAM wParam, 
                                            LPARAM lParam)
{
    // Get the object pointer.
    CPropSheetExt *pExt = (CPropSheetExt*)GetProp(hWnd, THIS_POINTER_PROP);
    
    switch(uMsg)
    {
    case WM_INITDIALOG:
        {
            /*
            Get the pointer to the object. This is contained in the LPARAM of 
            the PROPSHEETPAGE structure.
            */
            LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

            if(pPage)
            {
                pExt = (CPropSheetExt*)pPage->lParam;

                if(pExt)
                {
                    // Set the page window handle in the object.
                    pExt->m_hwndPage = hWnd;
                    
                    // Store the object pointer with this particular page dialog.
                    SetProp(hWnd, THIS_POINTER_PROP, (HANDLE)pExt);

                    ADsPropSetHwnd(pExt->m_hwndNotifyObj, hWnd, g_szPageTitle);

                    // Forward the message to the message handler.
                    return pExt->OnInitDialog(wParam, lParam);
                }
            }
        }
        break;

    case WM_NOTIFY:
        if(pExt)
        {
            // Forward the message to the message handler.
            return pExt->OnNotify(wParam, lParam);
        }
        break;
    
    case WM_COMMAND:
        if(pExt)
        {
            // Forward the message to the message handler.
            return pExt->OnCommand(wParam, lParam);
        }
        return FALSE;
    
    case WM_DESTROY:
        if(pExt)
        {
            // Forward the message to the message handler.
            pExt->OnDestroy();
        }
        
        // Remove the property from the page.
        RemoveProp(hWnd, THIS_POINTER_PROP);
        break; 
    }

    return FALSE;
}


/**************************************************************************

    CPropSheetExt::PageCallbackProc()

    This function is called when the page is created and released. This is 
    even called if the page is never actually displayed. 

**************************************************************************/

UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to create the page.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                if(IsWindow(pPropSheetExt->m_hwndNotifyObj))
                {
                    SendMessage(pPropSheetExt->m_hwndNotifyObj, 
                        WM_ADSPROP_NOTIFY_EXIT, 
                        0, 
                        0);

                    pPropSheetExt->m_hwndNotifyObj = NULL;
                }
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}


```



 

 