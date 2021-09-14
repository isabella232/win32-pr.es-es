---
title: Modificar código generado por el asistente
description: Modificar código generado por el asistente
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Reproductor de Windows Media Móvil, complementos
- Reproductor de Windows Media Dispositivos móviles, complementos de interfaz de usuario
- Reproductor de Windows Media Complementos móviles
- complementos, interfaz de usuario
- complementos, Reproductor de Windows Media Mobile
- complementos de interfaz de usuario, Reproductor de Windows Media Mobile
- Complementos de interfaz de usuario, Reproductor de Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359283"
---
# <a name="modifying-wizard-generated-code"></a>Modificar código generado por el asistente

Hay varios lugares en el código de complemento generado por el asistente que debe modificar para que el complemento funcione con Reproductor de Windows Media 10 Mobile. El código que debe modificar está en negrita en los ejemplos siguientes.

## <a name="changes-to-wmpplugh"></a>Cambios en wmpplug.h

Los métodos ANSI no se admiten en dispositivos que ejecutan Windows CE, por lo que debe modificar el siguiente método ANSI generado por el asistente en wmpplug.h:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Puede modificarlo como se muestra a continuación para que se convierta en un método Unicode:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Cambios en NetworkPlugin.h

Busque el código siguiente en NetworkPlugin.h:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Modifique el código para que sea similar al siguiente:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Cambios en NetworkPlugindll.cpp

Busque la **función DllMain** en NetworkPlugindll.cpp:


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



Modifique el código para que sea similar al siguiente:


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



## <a name="changes-to-networkplugincpp"></a>Cambios en NetworkPlugin.cpp

Busque el código siguiente en NetworkPlugin.cpp:


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Modifique el código para que sea similar al siguiente:


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Cambiar el modelo de subprocesos

A diferencia de ATL para Windows, ATL para Windows CE no admite el modelo de subprocesamiento de apartamento porque el modelo de apartamento requiere más recursos de memoria que los modelos de subprocesamiento único y subprocesamiento libre. Por lo tanto, debe encontrar todas las instancias de subprocesos de contenedor en StdAfx.h y NetworkPlugin.rgs y cambiarlas para indicar el subprocesamiento libre.

Además, solo puede llamar al control Reproductor de Windows Media 10 Mobile desde el subproceso en el que se creó.

## <a name="build-and-test-the-project"></a>Compilar y probar el Project

Después de realizar estos cambios descritos aquí, puede compilar el proyecto para comprobar que se compila antes de agregar cualquier código personalizado.

1.  Establezca la configuración del proyecto activo en La versión De depuración de Win32 (WCE ARMV4) o Win32 (WCE ARMV4).
2.  Establezca la plataforma activa en Pocket PC 2003.
3.  Haga clic en **el elemento** de menú Compilar y, a continuación, seleccione **Compilar NetworkPlugin.dll**. Debe compilar, descargar y registrarse en el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de Interfaz de usuario complemento para Reproductor de Windows Media 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




