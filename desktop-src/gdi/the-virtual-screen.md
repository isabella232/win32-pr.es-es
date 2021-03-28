---
description: El rectángulo delimitador de todos los monitores es la pantalla virtual. El escritorio cubre la pantalla virtual en lugar de un monitor único. En la ilustración siguiente se muestra una posible organización de tres monitores.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: La pantalla virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997929"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="523bb-105">La pantalla virtual</span><span class="sxs-lookup"><span data-stu-id="523bb-105">The Virtual Screen</span></span>

<span data-ttu-id="523bb-106">El rectángulo delimitador de todos los monitores es la *pantalla virtual*.</span><span class="sxs-lookup"><span data-stu-id="523bb-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="523bb-107">El escritorio cubre la pantalla virtual en lugar de un monitor único.</span><span class="sxs-lookup"><span data-stu-id="523bb-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="523bb-108">En la ilustración siguiente se muestra una posible organización de tres monitores.</span><span class="sxs-lookup"><span data-stu-id="523bb-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![Ilustración en la que se muestran tres cuadros que representan monitores organizados dentro de un cuadro que representa la pantalla virtual](images/multimon-1.png)

<span data-ttu-id="523bb-110">El *monitor principal* contiene el origen (0,0).</span><span class="sxs-lookup"><span data-stu-id="523bb-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="523bb-111">Esto es para la compatibilidad con las aplicaciones existentes que esperan un monitor con un origen.</span><span class="sxs-lookup"><span data-stu-id="523bb-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="523bb-112">Sin embargo, el monitor principal no tiene que estar en la parte superior izquierda de la pantalla virtual.</span><span class="sxs-lookup"><span data-stu-id="523bb-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="523bb-113">En la figura 1, está cerca del centro.</span><span class="sxs-lookup"><span data-stu-id="523bb-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="523bb-114">Cuando el monitor principal no está en la parte superior izquierda de la pantalla virtual, las partes de la pantalla virtual tienen coordenadas negativas.</span><span class="sxs-lookup"><span data-stu-id="523bb-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="523bb-115">Dado que el usuario establece la disposición de los monitores, todas las aplicaciones deben diseñarse para que funcionen con coordenadas negativas.</span><span class="sxs-lookup"><span data-stu-id="523bb-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="523bb-116">Para obtener más información, consulte [consideraciones de varios monitores para programas anteriores](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="523bb-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="523bb-117">Las coordenadas de la pantalla virtual se representan mediante un valor de 16 bits con signo debido a los valores de 16 bits contenidos en muchos mensajes existentes.</span><span class="sxs-lookup"><span data-stu-id="523bb-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="523bb-118">Por lo tanto, los límites de la pantalla virtual son:</span><span class="sxs-lookup"><span data-stu-id="523bb-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



