---
description: Los dos modos de asignación definidos por la aplicación (MM \_ anisotrópico y mm \_ ) se proporcionan para los modos de asignación específicos de la aplicación.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modos de asignación de Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997436"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="e836d-103">Modos de asignación de Application-Defined</span><span class="sxs-lookup"><span data-stu-id="e836d-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="e836d-104">Los dos modos de asignación definidos por la aplicación (MM \_ anisotrópico y mm \_ ) se proporcionan para los modos de asignación específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e836d-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="e836d-105">El \_ modo anisotrópico de mm garantiza que las unidades lógicas en la dirección x y en la dirección y son iguales, mientras que el \_ modo ANISOTRÓPICO de mm permite que las unidades difieran.</span><span class="sxs-lookup"><span data-stu-id="e836d-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="e836d-106">Una aplicación de CAD o de dibujo puede beneficiarse del modo de asignación de anisotrópico de MM \_ , pero puede que sea necesario especificar unidades lógicas que se correspondan con los incrementos de la escala de un ingeniero (1/64 de pulgada).</span><span class="sxs-lookup"><span data-stu-id="e836d-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="e836d-107">Estas unidades serían difíciles de obtener con los modos de asignación predefinidos (MM \_ HIENGLISH o mm \_ HIMETRIC); sin embargo, se pueden obtener fácilmente seleccionando el \_ modo anisotrópico de MM (o x \_ ).</span><span class="sxs-lookup"><span data-stu-id="e836d-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="e836d-108">En el ejemplo siguiente se muestra cómo establecer unidades lógicas en 1/64 pulgadas:</span><span class="sxs-lookup"><span data-stu-id="e836d-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



