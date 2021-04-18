---
title: booleano (WMI)
description: Es un \_ parámetro de VT bool que toma el valor de Variant \_ TRUE (&\# 8211; 1) o Variant \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706933"
---
# <a name="boolean-wmi"></a><span data-ttu-id="54b4a-103">booleano (WMI)</span><span class="sxs-lookup"><span data-stu-id="54b4a-103">boolean (WMI)</span></span>

<span data-ttu-id="54b4a-104">El tipo de datos Boolean es un \_ parámetro VT bool que toma el valor de Variant \_ true (– 1) o Variant \_ false (0).</span><span class="sxs-lookup"><span data-stu-id="54b4a-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="54b4a-105">En la tabla siguiente se muestra la diferencia entre las representaciones mediante programación de **true** lógico en C/C++ y el tipo de automatización.</span><span class="sxs-lookup"><span data-stu-id="54b4a-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="54b4a-106">Idioma</span><span class="sxs-lookup"><span data-stu-id="54b4a-106">Language</span></span>   | <span data-ttu-id="54b4a-107">Value</span><span class="sxs-lookup"><span data-stu-id="54b4a-107">Value</span></span>         | <span data-ttu-id="54b4a-108">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="54b4a-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="54b4a-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="54b4a-109">C/C++</span></span>      | <span data-ttu-id="54b4a-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="54b4a-110">**TRUE**</span></span>      | <span data-ttu-id="54b4a-111">1</span><span class="sxs-lookup"><span data-stu-id="54b4a-111">1</span></span>               |
| <span data-ttu-id="54b4a-112">Automatización</span><span class="sxs-lookup"><span data-stu-id="54b4a-112">Automation</span></span> | <span data-ttu-id="54b4a-113">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="54b4a-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="54b4a-114">–1</span><span class="sxs-lookup"><span data-stu-id="54b4a-114">–1</span></span>              |

<span data-ttu-id="54b4a-115">Ambos tipos son distintos de cero y, por lo tanto, no son **false**, pero tienen representaciones diferentes para **true**.</span><span class="sxs-lookup"><span data-stu-id="54b4a-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
