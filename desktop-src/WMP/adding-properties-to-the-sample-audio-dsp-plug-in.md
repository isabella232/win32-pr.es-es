---
title: Agregar propiedades al complemento DSP de audio de ejemplo
description: Agregar propiedades al complemento DSP de audio de ejemplo
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, propiedades de audio
- Complementos DSP, propiedades de audio
- Complementos DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695313"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="acf3e-108">Agregar propiedades al complemento DSP de audio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="acf3e-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="acf3e-109">El código de ejemplo de DSP de audio que genera el Asistente para complementos de Windows Media Player usa una única propiedad que representa el factor de escala para el volumen de audio.</span><span class="sxs-lookup"><span data-stu-id="acf3e-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="acf3e-110">El complemento puede requerir más de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="acf3e-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="acf3e-111">Puede agregar fácilmente propiedades al complemento DSP en Visual Studio siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="acf3e-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="acf3e-112">Defina los métodos en el código de definición de interfaz en el archivo IDL que forma parte del proyecto proxy-stub.</span><span class="sxs-lookup"><span data-stu-id="acf3e-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="acf3e-113">Agregue las implementaciones de método al archivo CPP principal del proyecto:</span><span class="sxs-lookup"><span data-stu-id="acf3e-113">Add the method implementations to the project's main CPP file:</span></span>

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

<span data-ttu-id="acf3e-114">Por último, para que el usuario pueda tener acceso a las propiedades, querrá realizar cambios en la implementación de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="acf3e-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acf3e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acf3e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf3e-116">**Implementar un complemento de DSP de audio**</span><span class="sxs-lookup"><span data-stu-id="acf3e-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




