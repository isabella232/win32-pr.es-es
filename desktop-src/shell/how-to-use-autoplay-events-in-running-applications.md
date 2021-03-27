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
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Cómo usar eventos de reproducción automática en aplicaciones en ejecución

La interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) se puede registrar en la tabla de objetos en ejecución (Rot) para que las aplicaciones en ejecución tengan acceso a los eventos de reproducción automática.

Las instrucciones siguientes describen cómo usar eventos de reproducción automática en aplicaciones en ejecución.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree un nuevo componente que implemente la interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

### <a name="step-2"></a>Paso 2:

Inicialice el nuevo componente con el valor InitCmdLine de la entrada del controlador en cuestión bajo la clave **handlers** .

Este paso es necesario porque la reproducción automática no llama al método Initialize.

### <a name="step-3"></a>Paso 3:

Llame a la función [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) para obtener un moniker que represente el componente y el controlador de eventos a los que desea llamar.

### <a name="step-4"></a>Paso 4:

Use el parámetro *ppmoniker* para registrar su componente en la tabla Rot.

## <a name="remarks"></a>Observaciones

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad. Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.

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

La llamada a [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiere que el componente tenga la siguiente información de **AppID** en el registro.

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

## <a name="related-topics"></a>Temas relacionados

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
