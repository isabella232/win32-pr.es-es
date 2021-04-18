---
title: Cambiar valores preestablecidos
description: Cambiar valores preestablecidos
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizaciones, muestra brillante
- visualizaciones personalizadas, ejemplo de resplandor
- Guía de programación, visualizaciones
- ejemplos, visualización de resplandor
- Ejemplo de visualización brillante
- visualizaciones, valores preestablecidos
- visualizaciones personalizadas, valores preestablecidos
- valores preestablecidos en visualizaciones, muestra brillante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695308"
---
# <a name="changing-presets"></a><span data-ttu-id="c3deb-111">Cambiar valores preestablecidos</span><span class="sxs-lookup"><span data-stu-id="c3deb-111">Changing Presets</span></span>

<span data-ttu-id="c3deb-112">Se cambiaron las siguientes secciones de código preestablecidas para permitir tres valores preestablecidos:</span><span class="sxs-lookup"><span data-stu-id="c3deb-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="c3deb-113">GetPresetTitle</span><span class="sxs-lookup"><span data-stu-id="c3deb-113">GetPresetTitle</span></span>

<span data-ttu-id="c3deb-114">Este código se insertó en lugar del código preestablecido generado:</span><span class="sxs-lookup"><span data-stu-id="c3deb-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="c3deb-115">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="c3deb-115">Enumerations</span></span>

<span data-ttu-id="c3deb-116">La siguiente enumeración en Glow. h se cambió para permitir tres valores preestablecidos:</span><span class="sxs-lookup"><span data-stu-id="c3deb-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="c3deb-117">Encabezado de recurso</span><span class="sxs-lookup"><span data-stu-id="c3deb-117">Resource Header</span></span>

<span data-ttu-id="c3deb-118">Los siguientes recursos se definieron en Resource. h para permitir tres valores preestablecidos:</span><span class="sxs-lookup"><span data-stu-id="c3deb-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="c3deb-119">Tenga en cuenta que también debe cambiar el número de recurso de **\_ APS \_ Next \_ SYMED \_ Value** por 106.</span><span class="sxs-lookup"><span data-stu-id="c3deb-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="c3deb-120">Archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="c3deb-120">Resource File</span></span>

<span data-ttu-id="c3deb-121">Las cadenas siguientes deben cambiarse en el archivo Glowdll. RC para permitir tres valores preestablecidos y asignarles nombres:</span><span class="sxs-lookup"><span data-stu-id="c3deb-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="c3deb-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3deb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3deb-123">**El ejemplo de resplandor**</span><span class="sxs-lookup"><span data-stu-id="c3deb-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




