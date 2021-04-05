---
title: Explorador de contenedor
description: Una aplicación puede usar la función DsBrowseForContainer para mostrar un cuadro de diálogo que se puede usar para examinar los contenedores de un servicio Dominio de Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- AD Container Browser
- contenedores AD, explorador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077552"
---
# <a name="container-browser"></a><span data-ttu-id="9f256-105">Explorador de contenedor</span><span class="sxs-lookup"><span data-stu-id="9f256-105">Container Browser</span></span>

<span data-ttu-id="9f256-106">Una aplicación puede usar la función [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para mostrar un cuadro de diálogo que se puede usar para examinar los contenedores de un servicio dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9f256-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="9f256-107">El cuadro de diálogo muestra los contenedores en formato de árbol y permite al usuario desplazarse por el árbol con el teclado y el mouse.</span><span class="sxs-lookup"><span data-stu-id="9f256-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="9f256-108">Cuando el usuario selecciona un elemento en el cuadro de diálogo, se proporciona el ADsPath del contenedor seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9f256-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="9f256-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) toma un puntero a una estructura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) que contiene datos sobre el cuadro de diálogo y devuelve el ADsPath del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9f256-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="9f256-110">El miembro **pszRoot** es un puntero a una cadena Unicode que contiene el contenedor raíz del árbol.</span><span class="sxs-lookup"><span data-stu-id="9f256-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="9f256-111">Si **pszRoot** es **null**, el árbol contendrá todo el árbol.</span><span class="sxs-lookup"><span data-stu-id="9f256-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="9f256-112">El miembro **pszPath** recibe el ADsPath del objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9f256-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="9f256-113">Es posible especificar que un contenedor determinado esté visible y seleccionado cuando se muestre por primera vez el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9f256-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="9f256-114">Esto se logra estableciendo **pszPath** en el ADsPath del elemento que se va a seleccionar y estableciendo la **marca \_ EXPANDONOPEN de DSBI** en **dwFlags**.</span><span class="sxs-lookup"><span data-stu-id="9f256-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="9f256-115">El contenido y el comportamiento del cuadro de diálogo también se pueden controlar en tiempo de ejecución mediante la implementación de una función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="9f256-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="9f256-116">La aplicación implementa la función **BFFCallBack** y se llama cuando se producen determinados eventos.</span><span class="sxs-lookup"><span data-stu-id="9f256-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="9f256-117">Una aplicación puede utilizar estos eventos para controlar el modo en que se muestran los elementos en el cuadro de diálogo, así como el contenido real del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9f256-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="9f256-118">Por ejemplo, una aplicación puede filtrar los elementos mostrados en el cuadro de diálogo implementando una función **BFFCallBack** que puede controlar la notificación de **\_ QUERYINSERT DSBM** .</span><span class="sxs-lookup"><span data-stu-id="9f256-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="9f256-119">Cuando se recibe una notificación de **\_ QUERYINSERT DSBM** , use el miembro **PszADsPath** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) para determinar qué elemento se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="9f256-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="9f256-120">Si la aplicación determina que el elemento no debe mostrarse, puede ocultar el elemento realizando los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9f256-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="9f256-121">Agregue la marca de **\_ Estado DSBF** al miembro **DwMask** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="9f256-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="9f256-122">Agregue la **marca \_ oculto DSBS** al miembro **DwStateMask** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="9f256-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="9f256-123">Agregue la **marca \_ oculto DSBS** al miembro **DwState** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="9f256-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="9f256-124">Devuelve un valor distinto de cero de la función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="9f256-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="9f256-125">Además de ocultar determinados elementos, una aplicación puede modificar el texto y el icono que se muestra para el elemento mediante el control de la notificación de **\_ QUERYINSERT DSBM** .</span><span class="sxs-lookup"><span data-stu-id="9f256-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="9f256-126">Para obtener más información, vea [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="9f256-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="9f256-127">La función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) puede usar la notificación de **BFFM \_ inicializada** para obtener el identificador del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9f256-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="9f256-128">La aplicación puede usar este identificador para enviar mensajes, como **BFFM \_ ENABLEOK**, al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9f256-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="9f256-129">Para obtener más información acerca de los mensajes que se pueden enviar al cuadro de diálogo, vea [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="9f256-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="9f256-130">El identificador del cuadro de diálogo también se puede utilizar para obtener acceso directo a los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9f256-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="9f256-131">**DSBID \_ BANNER** es el identificador del control de texto estático en el que se muestra el miembro **pszTitle** de la estructura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9f256-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="9f256-132">**DSBID \_ CONTAINERLIST** es el identificador del control de vista de árbol que se usa para mostrar el contenido del árbol.</span><span class="sxs-lookup"><span data-stu-id="9f256-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="9f256-133">El uso de estos elementos debe evitarse, si es posible, para evitar posibles problemas de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9f256-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="9f256-134">En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para crear el cuadro de diálogo explorador de contenedores e implementar una función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="9f256-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="9f256-135">[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa la notificación **de \_ QUERYINSERT DSBM** para cambiar el nombre para mostrar de cada elemento al nombre distintivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="9f256-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 