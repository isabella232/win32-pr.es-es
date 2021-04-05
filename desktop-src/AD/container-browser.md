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
# <a name="container-browser"></a>Explorador de contenedor

Una aplicación puede usar la función [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para mostrar un cuadro de diálogo que se puede usar para examinar los contenedores de un servicio dominio de Active Directory. El cuadro de diálogo muestra los contenedores en formato de árbol y permite al usuario desplazarse por el árbol con el teclado y el mouse. Cuando el usuario selecciona un elemento en el cuadro de diálogo, se proporciona el ADsPath del contenedor seleccionado por el usuario.

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) toma un puntero a una estructura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) que contiene datos sobre el cuadro de diálogo y devuelve el ADsPath del elemento seleccionado.

El miembro **pszRoot** es un puntero a una cadena Unicode que contiene el contenedor raíz del árbol. Si **pszRoot** es **null**, el árbol contendrá todo el árbol.

El miembro **pszPath** recibe el ADsPath del objeto seleccionado. Es posible especificar que un contenedor determinado esté visible y seleccionado cuando se muestre por primera vez el cuadro de diálogo. Esto se logra estableciendo **pszPath** en el ADsPath del elemento que se va a seleccionar y estableciendo la **marca \_ EXPANDONOPEN de DSBI** en **dwFlags**.

El contenido y el comportamiento del cuadro de diálogo también se pueden controlar en tiempo de ejecución mediante la implementación de una función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . La aplicación implementa la función **BFFCallBack** y se llama cuando se producen determinados eventos. Una aplicación puede utilizar estos eventos para controlar el modo en que se muestran los elementos en el cuadro de diálogo, así como el contenido real del cuadro de diálogo. Por ejemplo, una aplicación puede filtrar los elementos mostrados en el cuadro de diálogo implementando una función **BFFCallBack** que puede controlar la notificación de **\_ QUERYINSERT DSBM** . Cuando se recibe una notificación de **\_ QUERYINSERT DSBM** , use el miembro **PszADsPath** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) para determinar qué elemento se va a insertar. Si la aplicación determina que el elemento no debe mostrarse, puede ocultar el elemento realizando los pasos siguientes.

1.  Agregue la marca de **\_ Estado DSBF** al miembro **DwMask** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
2.  Agregue la **marca \_ oculto DSBS** al miembro **DwStateMask** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
3.  Agregue la **marca \_ oculto DSBS** al miembro **DwState** de la estructura [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
4.  Devuelve un valor distinto de cero de la función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .

Además de ocultar determinados elementos, una aplicación puede modificar el texto y el icono que se muestra para el elemento mediante el control de la notificación de **\_ QUERYINSERT DSBM** . Para obtener más información, vea [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

La función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) puede usar la notificación de **BFFM \_ inicializada** para obtener el identificador del cuadro de diálogo. La aplicación puede usar este identificador para enviar mensajes, como **BFFM \_ ENABLEOK**, al cuadro de diálogo. Para obtener más información acerca de los mensajes que se pueden enviar al cuadro de diálogo, vea [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

El identificador del cuadro de diálogo también se puede utilizar para obtener acceso directo a los controles del cuadro de diálogo. **DSBID \_ BANNER** es el identificador del control de texto estático en el que se muestra el miembro **pszTitle** de la estructura [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) . **DSBID \_ CONTAINERLIST** es el identificador del control de vista de árbol que se usa para mostrar el contenido del árbol. El uso de estos elementos debe evitarse, si es posible, para evitar posibles problemas de compatibilidad de aplicaciones.

En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) para crear el cuadro de diálogo explorador de contenedores e implementar una función [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) usa la notificación **de \_ QUERYINSERT DSBM** para cambiar el nombre para mostrar de cada elemento al nombre distintivo del elemento.


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



 

 