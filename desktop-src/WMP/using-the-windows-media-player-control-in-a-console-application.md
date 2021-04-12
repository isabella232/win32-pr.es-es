---
title: Usar el control de Media Player de Windows en una aplicación de consola
description: Usar el control de Media Player de Windows en una aplicación de consola
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, aplicaciones de consola
- Modelo de objetos de Windows Media Player, aplicaciones de consola
- modelo de objetos, aplicaciones de consola
- Windows Media Player Mobile, aplicaciones de consola
- Control ActiveX de Windows Media Player, aplicaciones de consola
- Control ActiveX móvil de Windows Media Player, aplicaciones de consola
- Control ActiveX, aplicaciones de consola
- inserción de aplicación de consola
- incrustación, aplicaciones de consola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357279"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a><span data-ttu-id="a6f4b-119">Usar el control de Media Player de Windows en una aplicación de consola</span><span class="sxs-lookup"><span data-stu-id="a6f4b-119">Using the Windows Media Player Control in a Console Application</span></span>

<span data-ttu-id="a6f4b-120">Puede crear una instancia del objeto COM de Windows Media Player directamente mediante **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-120">You can create an instance of the Windows Media Player COM object directly by using **CoCreateInstance**.</span></span> <span data-ttu-id="a6f4b-121">Al hacerlo, el objeto **Player** no muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-121">When you do this, the **Player** object displays no user interface.</span></span> <span data-ttu-id="a6f4b-122">Sin embargo, el objeto sigue siendo útil para las tareas que no requieren la interfaz de usuario, como el trabajo con la biblioteca, la reproducción de archivos de audio digital o el acceso a las propiedades del reproductor.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-122">However, the object is still useful for tasks that don't require the user interface, such as working with the library, playing digital audio files, or accessing properties of the Player.</span></span>

<span data-ttu-id="a6f4b-123">En el ejemplo de código siguiente se muestra un programa de consola simple que muestra la versión de Windows Media Player en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-123">The following example code shows a simple console program that displays the Windows Media Player version in a message box.</span></span> <span data-ttu-id="a6f4b-124">En el código de ejemplo se utiliza ATL para aprovechar las ventajas de los punteros inteligentes y la clase de cadena **CComBSTR** .</span><span class="sxs-lookup"><span data-stu-id="a6f4b-124">The example code uses ATL to take advantage of smart pointers and the **CComBSTR** string class.</span></span>


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="a6f4b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6f4b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f4b-126">**Usar el control Media Player de Windows en un programa de C++**</span><span class="sxs-lookup"><span data-stu-id="a6f4b-126">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




