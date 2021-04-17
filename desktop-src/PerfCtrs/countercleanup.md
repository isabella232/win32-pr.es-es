---
description: Quita el registro de proveedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Función de limpieza
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667341"
---
# <a name="countercleanup-function"></a><span data-ttu-id="fc8ea-103">Función de limpieza</span><span class="sxs-lookup"><span data-stu-id="fc8ea-103">CounterCleanup function</span></span>

<span data-ttu-id="fc8ea-104">Quita el registro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc8ea-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="fc8ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc8ea-106">Parameters</span></span>

<span data-ttu-id="fc8ea-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc8ea-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc8ea-108">Return value</span></span>

<span data-ttu-id="fc8ea-109">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8ea-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc8ea-110">Remarks</span></span>

<span data-ttu-id="fc8ea-111">El proveedor llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-111">Your provider calls this function.</span></span> <span data-ttu-id="fc8ea-112">La función llama a la función [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="fc8ea-113">La herramienta [**CTRPP**](ctrpp.md) genera esta función insertada al especificar el argumento **-o** .</span><span class="sxs-lookup"><span data-stu-id="fc8ea-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="fc8ea-114">El nombre de la función incluye una cadena de *prefijo* si se especifica el argumento **-prefix** (por ejemplo, **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="fc8ea-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8ea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc8ea-115">Requirements</span></span>



| <span data-ttu-id="fc8ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8ea-116">Requirement</span></span> | <span data-ttu-id="fc8ea-117">Value</span><span class="sxs-lookup"><span data-stu-id="fc8ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fc8ea-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8ea-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc8ea-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fc8ea-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8ea-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc8ea-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




