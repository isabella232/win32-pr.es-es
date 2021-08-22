---
title: Cómo usar OLE en controles Rich Edit
description: Esta sección contiene información sobre el uso de la vinculación e inserción de objetos (OLE) en controles de edición enriquecidos.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d825a9876005cadb20e4fc7717f766582ab12224f4f86995319357875d24230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311685"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Cómo usar OLE en controles Rich Edit

Esta sección contiene información sobre el uso de la vinculación e inserción de objetos (OLE) en controles de edición enriquecidos.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-interface"></a>Usar una interfaz rich edit

Los controles de edición enriquecciones exponen parte de su funcionalidad a través de interfaces de Modelo de objetos componentes (COM). Al obtener una interfaz de un control, se obtiene la capacidad de trabajar con otros objetos dentro del control . Puede obtener esta interfaz mediante el envío del [**mensaje EM \_ GETOLEINTERFACE.**](em-getoleinterface.md) Desde la [**interfaz IRichEditOle,**](/windows/desktop/api/Richole/nn-richole-iricheditole) puede obtener las interfaces usadas en el modelo [de objetos de texto](text-object-model.md).

Las aplicaciones implementan otra interfaz, [**IRichEditOleCallback,**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)para definir el comportamiento del control cuando interactúa con objetos .

### <a name="insert-an-object-into-a-rich-edit-control"></a>Insertar un objeto en un control Rich Edit

En el ejemplo de código siguiente se inserta un objeto de archivo en un control de edición enriquecido. Si un programa está asociado al tipo de archivo en el equipo del usuario (por ejemplo, Microsoft Excel para un archivo .xls), el contenido del archivo se muestra en el control ; De lo contrario, aparece un icono.

1.  Obtenga la [**interfaz IRichEditOle.**](/windows/desktop/api/Richole/nn-richole-iricheditole)

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Cree almacenamiento estructurado.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Configure el formato de datos.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Obtenga un puntero al sitio para mostrar.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Cree el objeto y recupere su **interfaz IUnknown.**

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  Obtenga la interfaz IOleObject para el objeto .

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Para asegurarse de que las referencias se cuentan correctamente, notifique al objeto que está contenido.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Configure la información del objeto.

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  Mueva el elemento de careta al final del texto y agregue un retorno de carro.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Inserte el objeto .

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Limpiar.

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Uso de IRichEditOleCallback

Las aplicaciones implementan [**la interfaz IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) para responder a las consultas o acciones relacionadas con OLE realizadas por un control de edición enriquecido. Asocie la implementación de la interfaz con el control mediante el envío de un [**mensaje EM \_ SETOLECALLBACK.**](em-setolecallback.md) A continuación, el control llama a métodos en la implementación de la interfaz según corresponda.

Por ejemplo, [**se llama a QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) cuando el usuario intenta arrastrar o pegar un objeto en el control . Si la aplicación puede aceptar los datos, la implementación del método devuelve S \_ OK; de lo contrario, devuelve un código de error. El método también puede realizar alguna otra acción, como advertir al usuario de que los archivos de ese tipo no se pueden colocar en el control .

## <a name="complete-insertobject-example-function"></a>Función de ejemplo InsertObject completa

En el ejemplo de código siguiente se muestran los fragmentos de código anteriores combinados en una función completa que incluye el control de errores.


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




