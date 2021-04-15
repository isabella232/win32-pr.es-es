---
title: Modificar el código generado por el asistente
description: Modificar el código generado por el asistente
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player Mobile, Complementos
- Windows Media Player Mobile, Complementos de la interfaz de usuario
- Complementos móviles de Windows Media Player
- complementos, interfaz de usuario
- complementos, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695416"
---
# <a name="modifying-wizard-generated-code"></a>Modificar el código generado por el asistente

Hay varios lugares en el código de complemento generado por el asistente que debe modificar antes de que el complemento funcione con Windows Media Player 10 Mobile. El código que debe modificar está en negrita en los ejemplos siguientes.

## <a name="changes-to-wmpplugh"></a>Cambios en wmpplug. h

Los métodos ANSI no se admiten en los dispositivos que ejecutan Windows CE, por lo que debe modificar el siguiente método ANSI generado por el asistente en wmpplug. h:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Modifíquelo como se muestra a continuación para que se convierta en un método Unicode:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Cambios en NetworkPlugin. h

Busque el siguiente código en NetworkPlugin. h:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Modifique el código para que tenga el aspecto siguiente:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Cambios en NetworkPlugindll. cpp

Busque la función **DllMain** en NetworkPlugindll. cpp:


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



Modifique el código para que tenga el aspecto siguiente:


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>Cambios en NetworkPlugin. cpp

Busque el siguiente código en NetworkPlugin. cpp:


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Modifique el código para que tenga el aspecto siguiente:


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Cambiar el modelo de subprocesos

A diferencia de ATL para Windows, ATL para Windows CE no es compatible con el modelo de subprocesos de Apartamento porque el modelo de Apartamento requiere más recursos de memoria que los modelos de subprocesamiento único y de subprocesamiento libre. Por lo tanto, debe buscar todas las instancias de subprocesamiento de apartamento en StdAfx. h y NetworkPlugin. RGS y cambiarlas para indicar el subprocesamiento libre.

Además, solo puede llamar al control de Windows Media Player 10 Mobile desde el subproceso en el que se creó.

## <a name="build-and-test-the-project"></a>Compilar y probar el proyecto

Después de realizar estos cambios, puede compilar el proyecto para comprobar que se compila antes de agregar cualquier código personalizado.

1.  Establezca la configuración del proyecto activo en Win32 (WCE ARMV4) debug o Win32 (WCE ARMV4).
2.  Establezca la plataforma activa en Pocket PC 2003.
3.  Haga clic en el elemento de menú **compilar** y, a continuación, seleccione **compilar NetworkPlugin.dll**. Debe compilar, descargar y registrarse en el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




