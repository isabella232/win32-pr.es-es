---
title: Hospedar el control de Media Player de Windows en una aplicación de Windows
description: Hospedar el control de Media Player de Windows en una aplicación de Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, programas basados en Windows
- Modelo de objetos de Windows Media Player, programas basados en Windows
- modelo de objetos, programas basados en Windows
- Windows Media Player dispositivos móviles y basados en Windows
- Control ActiveX de Windows Media Player, programas basados en Windows
- Control ActiveX móvil de Windows Media Player, programas basados en Windows
- Control ActiveX, programas basados en Windows
- Inserción de programas basados en Windows
- incrustación, programas basados en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357466"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hospedar el control de Media Player de Windows en una aplicación de Windows

Para usar el control ActiveX de Windows Media Player (incluida la interfaz de usuario) en un programa basado en Windows, debe proporcionar un contenedor de controles ActiveX. ATL proporciona la clase **CAxWindow** para proporcionar la funcionalidad de la ventana host de ActiveX.

Para hospedar el control de Media Player de Windows mediante la clase **CAxWindow** , siga estos pasos:

1.  Incluya los encabezados siguientes:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Declare las variables de miembro, como se indica a continuación:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Cuando se cree la ventana de la aplicación, llame a **AtlAxWinInit**, que es necesario cuando se usa la ventana host ActiveX ATL.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Declare las variables locales para los códigos de retorno y contenga el puntero a la interfaz de la ventana host:
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

    

7.  Cree el control Media Player de Windows en la ventana host con el ID. de clase:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recupere el puntero de la interfaz **IWMPPlayer** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Al escribir su propio código, asegúrese de comprobar si hay errores en cada código de retorno **HRESULT** .

Para obtener un ejemplo completo que muestra cómo hospedar el control ActiveX de Windows Media Player mediante la clase **CAxWindow** , vea el ejemplo WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hospedar el control de Windows Media Player 10 Mobile en Windows CE

Microsoft eMbedded Visual C++ 4,0 y el SDK de Pocket PC 2003 o el SDK de smartphone 2003 deben instalarse al desarrollar aplicaciones basadas en Windows CE que hospeden un control de Windows Media Player 10 Mobile. Además, a diferencia de ATL para Windows, ATL para Windows CE no admite el modelo de subprocesos de apartamento. Por lo tanto, debe buscar todas las instancias de subprocesamiento de apartamento en el proyecto ATL y cambiarlas para usar el subprocesamiento libre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




