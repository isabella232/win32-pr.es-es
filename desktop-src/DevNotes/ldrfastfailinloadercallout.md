---
description: Esta función finaliza forzosamente el programa de llamada si se invoca dentro de una llamada del cargador. De lo contrario, no tiene ningún efecto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670416"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="e992a-104">LdrFastFailInLoaderCallout función)</span><span class="sxs-lookup"><span data-stu-id="e992a-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="e992a-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e992a-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e992a-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e992a-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e992a-107">Esta función finaliza forzosamente el programa de llamada si se invoca dentro de una llamada del cargador.</span><span class="sxs-lookup"><span data-stu-id="e992a-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="e992a-108">De lo contrario, no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="e992a-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e992a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e992a-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="e992a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e992a-110">Parameters</span></span>

<span data-ttu-id="e992a-111">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e992a-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e992a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e992a-112">Return value</span></span>

<span data-ttu-id="e992a-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e992a-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e992a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e992a-114">Remarks</span></span>

<span data-ttu-id="e992a-115">Esta rutina no detecta todos los posibles casos de interbloqueo; es posible que un subproceso dentro de una llamada del cargador adquiera un bloqueo mientras que un subproceso fuera de una llamada del cargador contiene el mismo bloqueo y realiza una llamada al cargador.</span><span class="sxs-lookup"><span data-stu-id="e992a-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="e992a-116">En otras palabras, puede haber una inversión del orden de bloqueo entre el bloqueo del cargador y un bloqueo de cliente.</span><span class="sxs-lookup"><span data-stu-id="e992a-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="e992a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e992a-117">Requirements</span></span>



| <span data-ttu-id="e992a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e992a-118">Requirement</span></span> | <span data-ttu-id="e992a-119">Value</span><span class="sxs-lookup"><span data-stu-id="e992a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e992a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e992a-120">Library</span></span><br/> | <dl> <span data-ttu-id="e992a-121"><dt>NTDll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e992a-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="e992a-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e992a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e992a-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e992a-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




