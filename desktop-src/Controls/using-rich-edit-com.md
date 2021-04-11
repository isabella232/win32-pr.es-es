---
title: Cómo usar OLE en controles Rich Edit
description: Esta sección contiene información acerca del uso de la vinculación e incrustación de objetos (OLE) en controles Rich Edit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104149143"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="9f832-103">Cómo usar OLE en controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9f832-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="9f832-104">Esta sección contiene información acerca del uso de la vinculación e incrustación de objetos (OLE) en controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9f832-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9f832-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="9f832-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9f832-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="9f832-106">Technologies</span></span>

-   [<span data-ttu-id="9f832-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="9f832-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9f832-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f832-108">Prerequisites</span></span>

-   <span data-ttu-id="9f832-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="9f832-109">C/C++</span></span>
-   <span data-ttu-id="9f832-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="9f832-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9f832-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="9f832-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="9f832-112">Usar una interfaz de edición enriquecida</span><span class="sxs-lookup"><span data-stu-id="9f832-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="9f832-113">Los controles Rich Edit exponen parte de su funcionalidad a través de las interfaces del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="9f832-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="9f832-114">Al obtener una interfaz de un control, se obtiene la capacidad de trabajar con otros objetos en el control.</span><span class="sxs-lookup"><span data-stu-id="9f832-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="9f832-115">Puede obtener esta interfaz enviando el mensaje [**\_ GETOLEINTERFACE em**](em-getoleinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="9f832-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="9f832-116">En la interfaz [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) , puede obtener las interfaces usadas en el [modelo de objetos de texto](text-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9f832-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="9f832-117">Otra interfaz, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), se implementa mediante aplicaciones para definir el comportamiento del control cuando interactúa con objetos.</span><span class="sxs-lookup"><span data-stu-id="9f832-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="9f832-118">Insertar un objeto en un control Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9f832-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="9f832-119">En el ejemplo de código siguiente se inserta un objeto de archivo en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9f832-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="9f832-120">Si un programa está asociado al tipo de archivo en el equipo del usuario (por ejemplo, Microsoft Excel para un archivo. xls), el contenido del archivo se muestra en el control; de lo contrario, aparece un icono.</span><span class="sxs-lookup"><span data-stu-id="9f832-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="9f832-121">Obtiene la interfaz [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="9f832-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="9f832-122">Crear almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="9f832-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="9f832-123">Configure el formato de datos.</span><span class="sxs-lookup"><span data-stu-id="9f832-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="9f832-124">Obtiene un puntero al sitio para mostrar.</span><span class="sxs-lookup"><span data-stu-id="9f832-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="9f832-125">Cree el objeto y recupere su interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9f832-125">Create the object and retrieve its **IUnknown** interface.</span></span>

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

    

6.  <span data-ttu-id="9f832-126">Obtiene la interfaz IOleObject para el objeto.</span><span class="sxs-lookup"><span data-stu-id="9f832-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="9f832-127">Para asegurarse de que las referencias se cuentan correctamente, notifique al objeto que está incluida.</span><span class="sxs-lookup"><span data-stu-id="9f832-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="9f832-128">Configure la información del objeto.</span><span class="sxs-lookup"><span data-stu-id="9f832-128">Set up object info.</span></span>

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

    

9.  <span data-ttu-id="9f832-129">Mueve el símbolo de intercalación hasta el final del texto y agrega un retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="9f832-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="9f832-130">Inserte el objeto.</span><span class="sxs-lookup"><span data-stu-id="9f832-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="9f832-131">Limpiar.</span><span class="sxs-lookup"><span data-stu-id="9f832-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="9f832-132">Usar IRichEditOleCallback</span><span class="sxs-lookup"><span data-stu-id="9f832-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="9f832-133">Las aplicaciones implementan la interfaz [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) para responder a las consultas o acciones relacionadas con OLE realizadas por un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9f832-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="9f832-134">Puede asociar la implementación de la interfaz con el control mediante el envío de un mensaje [**\_ SETOLECALLBACK em**](em-setolecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="9f832-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="9f832-135">A continuación, el control llama a los métodos en la implementación de la interfaz según corresponda.</span><span class="sxs-lookup"><span data-stu-id="9f832-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="9f832-136">Por ejemplo, se llama a [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) cuando el usuario intenta arrastrar o pegar un objeto en el control.</span><span class="sxs-lookup"><span data-stu-id="9f832-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="9f832-137">Si la aplicación puede aceptar los datos, la implementación del método devuelve S \_ correcto; de lo contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="9f832-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="9f832-138">El método también puede realizar alguna otra acción, como advertir al usuario de que no se pueden colocar archivos de ese tipo en el control.</span><span class="sxs-lookup"><span data-stu-id="9f832-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="9f832-139">Función de ejemplo InsertObject completa</span><span class="sxs-lookup"><span data-stu-id="9f832-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="9f832-140">En el ejemplo de código siguiente se muestran los fragmentos de código anteriores combinados en una función completa que incluye el control de errores.</span><span class="sxs-lookup"><span data-stu-id="9f832-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9f832-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f832-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f832-142">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9f832-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="9f832-143">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9f832-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




