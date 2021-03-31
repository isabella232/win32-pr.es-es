---
description: Siga estas instrucciones al crear un módulo de combinación de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Usar módulos de combinación de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815430"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="a9590-103">Usar módulos de combinación de 64 bits</span><span class="sxs-lookup"><span data-stu-id="a9590-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="a9590-104">Un módulo de combinación de 64 bits tiene cualquiera de las características que se identifican en este tema.</span><span class="sxs-lookup"><span data-stu-id="a9590-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="a9590-105">El módulo de combinación contiene al menos un componente que se ha compilado para los sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a9590-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="a9590-106">El módulo de combinación no contiene componentes de 64 bits, pero está pensado para usarse solo con paquetes de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="a9590-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="a9590-107">Los módulos de combinación se pueden usar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a9590-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="a9590-108">Un módulo de combinación de 64 bits se puede combinar en un paquete de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="a9590-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="a9590-109">Las propiedades de Resumen de la [**plantilla**](template-summary.md) en el módulo de combinación y en el paquete de Windows Installer se deben establecer en el mismo tipo de procesador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a9590-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="a9590-110">Un módulo de fusión mediante combinación x64 solo se puede combinar en paquetes x64 y un módulo Intel64 Merge solo se puede combinar en paquetes de Intel64.</span><span class="sxs-lookup"><span data-stu-id="a9590-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="a9590-111">Un módulo de combinación de 32 bits se puede combinar en paquetes de Windows Installer de 32 bits o [de 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="a9590-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="a9590-112">Un módulo de combinación de 64 bits se puede combinar en un paquete de 64 bits en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a9590-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="a9590-113">Al crear un módulo de combinación de 64 bits, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a9590-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="a9590-114">Utilice el mismo procedimiento general que al crear módulos de combinación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a9590-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="a9590-115">Para obtener más información, vea acerca de los [módulos de combinación](about-merge-modules.md) y de creación de [módulos de combinación](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a9590-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="a9590-116">Debe establecer la propiedad de Resumen de la [**plantilla**](template-summary.md) con el valor Intel64 si se ejecuta un sistema Intel64.</span><span class="sxs-lookup"><span data-stu-id="a9590-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="a9590-117">Debe establecer la propiedad de Resumen de la **plantilla** con el valor x64 si ejecuta un sistema x64.</span><span class="sxs-lookup"><span data-stu-id="a9590-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="a9590-118">Para obtener más información, vea [referencia de flujo de información de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a9590-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="a9590-119">Cuando existen módulos de combinación de 32 y 64 bits para el mismo componente, se recomienda que los módulos tengan firmas diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9590-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="a9590-120">Esto permitirá que un paquete contenga ambas versiones del componente.</span><span class="sxs-lookup"><span data-stu-id="a9590-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="a9590-121">Para obtener más información, consulte [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="a9590-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



