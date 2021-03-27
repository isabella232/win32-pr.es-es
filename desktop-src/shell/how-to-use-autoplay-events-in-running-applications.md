---
description: La interfaz IHWEventHandler se puede registrar en la tabla de objetos en ejecución (ROT) para que las aplicaciones en ejecución tengan acceso a los eventos de reproducción automática.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Cómo usar eventos de reproducción automática en aplicaciones en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001900"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="a966d-103">Cómo usar eventos de reproducción automática en aplicaciones en ejecución</span><span class="sxs-lookup"><span data-stu-id="a966d-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="a966d-104">La interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) se puede registrar en la tabla de objetos en ejecución (Rot) para que las aplicaciones en ejecución tengan acceso a los eventos de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="a966d-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="a966d-105">Las instrucciones siguientes describen cómo usar eventos de reproducción automática en aplicaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="a966d-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="a966d-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a966d-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a966d-107">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="a966d-107">Step 1:</span></span>

<span data-ttu-id="a966d-108">Cree un nuevo componente que implemente la interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="a966d-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="a966d-109">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="a966d-109">Step 2:</span></span>

<span data-ttu-id="a966d-110">Inicialice el nuevo componente con el valor InitCmdLine de la entrada del controlador en cuestión bajo la clave **handlers** .</span><span class="sxs-lookup"><span data-stu-id="a966d-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="a966d-111">Este paso es necesario porque la reproducción automática no llama al método Initialize.</span><span class="sxs-lookup"><span data-stu-id="a966d-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="a966d-112">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="a966d-112">Step 3:</span></span>

<span data-ttu-id="a966d-113">Llame a la función [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) para obtener un moniker que represente el componente y el controlador de eventos a los que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="a966d-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="a966d-114">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="a966d-114">Step 4:</span></span>

<span data-ttu-id="a966d-115">Use el parámetro *ppmoniker* para registrar su componente en la tabla Rot.</span><span class="sxs-lookup"><span data-stu-id="a966d-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="a966d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a966d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a966d-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="a966d-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="a966d-118">Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a966d-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

<span data-ttu-id="a966d-119">La llamada a [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiere que el componente tenga la siguiente información de **AppID** en el registro.</span><span class="sxs-lookup"><span data-stu-id="a966d-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a><span data-ttu-id="a966d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a966d-120">Related topics</span></span>

[<span data-ttu-id="a966d-121">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="a966d-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="a966d-122">**CreateHardwareEventMoniker**</span><span class="sxs-lookup"><span data-stu-id="a966d-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
