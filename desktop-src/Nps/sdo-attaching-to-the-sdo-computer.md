---
title: Asociar al equipo SDO
description: Con el puntero de interfaz devuelto por CoCreateInstance, llame al método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995330"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="7f13b-103">Asociar al equipo SDO</span><span class="sxs-lookup"><span data-stu-id="7f13b-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="7f13b-104">Con el puntero de interfaz devuelto por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), llame al método [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) .</span><span class="sxs-lookup"><span data-stu-id="7f13b-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="7f13b-105">Pase **null** como parámetro al método **Attach** .</span><span class="sxs-lookup"><span data-stu-id="7f13b-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="7f13b-106">El valor **null** especifica que **Attach** asocia el objeto de equipo con el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7f13b-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="7f13b-107">No se admite la asociación a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="7f13b-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="7f13b-108">Para determinar si el equipo local ya está adjunto, llame al método [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .</span><span class="sxs-lookup"><span data-stu-id="7f13b-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="7f13b-109">Vea [asociar a un SDO-Enabled equipo](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver el código de ejemplo que muestra cómo conectarse al equipo local.</span><span class="sxs-lookup"><span data-stu-id="7f13b-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 