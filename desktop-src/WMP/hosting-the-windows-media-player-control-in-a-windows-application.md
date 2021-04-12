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
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="ac19f-119">Hospedar el control de Media Player de Windows en una aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="ac19f-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="ac19f-120">Para usar el control ActiveX de Windows Media Player (incluida la interfaz de usuario) en un programa basado en Windows, debe proporcionar un contenedor de controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ac19f-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="ac19f-121">ATL proporciona la clase **CAxWindow** para proporcionar la funcionalidad de la ventana host de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ac19f-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="ac19f-122">Para hospedar el control de Media Player de Windows mediante la clase **CAxWindow** , siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ac19f-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="ac19f-123">Incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="ac19f-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="ac19f-124">Declare las variables de miembro, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ac19f-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="ac19f-125">Cuando se cree la ventana de la aplicación, llame a **AtlAxWinInit**, que es necesario cuando se usa la ventana host ActiveX ATL.</span><span class="sxs-lookup"><span data-stu-id="ac19f-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="ac19f-126">Declare las variables locales para los códigos de retorno y contenga el puntero a la interfaz de la ventana host:</span><span class="sxs-lookup"><span data-stu-id="ac19f-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="ac19f-127">Cree la ventana host:</span><span class="sxs-lookup"><span data-stu-id="ac19f-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="ac19f-128">Recupere el puntero de interfaz de la ventana host:</span><span class="sxs-lookup"><span data-stu-id="ac19f-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="ac19f-129">Cree el control Media Player de Windows en la ventana host con el ID. de clase:</span><span class="sxs-lookup"><span data-stu-id="ac19f-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="ac19f-130">Recupere el puntero de la interfaz **IWMPPlayer** :</span><span class="sxs-lookup"><span data-stu-id="ac19f-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="ac19f-131">Al escribir su propio código, asegúrese de comprobar si hay errores en cada código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac19f-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="ac19f-132">Para obtener un ejemplo completo que muestra cómo hospedar el control ActiveX de Windows Media Player mediante la clase **CAxWindow** , vea el ejemplo WMPHost.</span><span class="sxs-lookup"><span data-stu-id="ac19f-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="ac19f-133">Hospedar el control de Windows Media Player 10 Mobile en Windows CE</span><span class="sxs-lookup"><span data-stu-id="ac19f-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="ac19f-134">Microsoft eMbedded Visual C++ 4,0 y el SDK de Pocket PC 2003 o el SDK de smartphone 2003 deben instalarse al desarrollar aplicaciones basadas en Windows CE que hospeden un control de Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="ac19f-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="ac19f-135">Además, a diferencia de ATL para Windows, ATL para Windows CE no admite el modelo de subprocesos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="ac19f-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="ac19f-136">Por lo tanto, debe buscar todas las instancias de subprocesamiento de apartamento en el proyecto ATL y cambiarlas para usar el subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="ac19f-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac19f-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac19f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac19f-138">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="ac19f-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="ac19f-139">**Usar el control Media Player de Windows en un programa de C++**</span><span class="sxs-lookup"><span data-stu-id="ac19f-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




