---
title: Varios controles en un archivo DLL
description: Varios controles en un archivo DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075154"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="32a89-103">Varios controles en un archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32a89-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="32a89-104">Un solo archivo DLL. ocx puede incluir cualquier número de controles ActiveX, lo que simplifica la distribución y el uso de un conjunto de controles relacionados.</span><span class="sxs-lookup"><span data-stu-id="32a89-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="32a89-105">Si envía varios controles a un solo archivo DLL, asegúrese de incluir el nombre del proveedor en cada nombre de control del paquete.</span><span class="sxs-lookup"><span data-stu-id="32a89-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="32a89-106">La inclusión de los nombres de los proveedores en cada nombre de control permitirá a los usuarios identificar fácilmente los controles dentro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="32a89-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="32a89-107">Por ejemplo, si envía un archivo DLL que implementa tres controles, Con1, Con2 y Con3, los nombres de los controles deben ser:</span><span class="sxs-lookup"><span data-stu-id="32a89-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="32a89-108">*El nombre de la empresa* Control Con1</span><span class="sxs-lookup"><span data-stu-id="32a89-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="32a89-109">*El nombre de la empresa* Control Con2</span><span class="sxs-lookup"><span data-stu-id="32a89-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="32a89-110">*El nombre de la empresa* Control Con3</span><span class="sxs-lookup"><span data-stu-id="32a89-110">*Your company name* Con3 Control</span></span>

 

 




