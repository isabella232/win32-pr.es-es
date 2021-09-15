---
title: Hospedar el control Reproductor de Windows Media en una Windows aplicación
description: Hospedar el control Reproductor de Windows Media en una Windows aplicación
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,Windows basados en aplicaciones
- Reproductor de Windows Media de objetos, Windows basados en objetos
- modelo de objetos, Windows basados en objetos
- Reproductor de Windows Media Programas basados Windows móviles
- Reproductor de Windows Media ActiveX control de Windows basados en aplicaciones
- Reproductor de Windows Media Control de ActiveX móviles, Windows basados en dispositivos móviles
- ActiveX control de Windows basados en aplicaciones
- Windows inserción de programas basados en archivos
- inserción, Windows basados en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476240"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hospedar el control Reproductor de Windows Media en una Windows aplicación

Para usar el control Reproductor de Windows Media ActiveX (incluida la interfaz de usuario) en un programa basado en Windows, debe proporcionar un contenedor ActiveX control. ATL proporciona la **clase CAxWindow para** proporcionar ActiveX de ventana host.

Para hospedar el control Reproductor de Windows Media mediante la **clase CAxWindow,** siga estos pasos:

1.  Incluya los encabezados siguientes:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Declare variables miembro, como se muestra a continuación:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Cuando se crea la ventana de aplicación, llame **a AtlAxWinInit**, que es necesario cuando se usa la ventana ActiveX atl.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Declare variables locales para los códigos de retorno y para que contengan el puntero a la interfaz de ventana host:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Cree la ventana host:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Recupere el puntero de interfaz de la ventana host:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Cree el control Reproductor de Windows Media en la ventana host mediante el identificador de clase:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recupere el **puntero de interfaz IWMPPlayer:**
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Al escribir su propio código, asegúrese de comprobar si hay errores en cada **código devuelto HRESULT.**

Para obtener un ejemplo completo que muestra cómo hospedar el control Reproductor de Windows Media ActiveX mediante la **clase CAxWindow,** vea el ejemplo WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hospedaje del control Reproductor de Windows Media 10 Mobile en Windows CE

Microsoft eMbedded Visual C++ 4.0 y el SDK de Pocket PC 2003 o el SDK de Smartphone 2003 deben instalarse al desarrollar aplicaciones basadas en Windows CE que hospedan un control Reproductor de Windows Media 10 Mobile. Además, a diferencia de ATL para Windows, ATL para Windows CE no admite el modelo de subprocesos de apartamento. Por lo tanto, debe buscar todas las instancias de subprocesos de contenedor en el proyecto ATL y cambiarlas para que usen el subprocesamiento libre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Muestras**](samples.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




