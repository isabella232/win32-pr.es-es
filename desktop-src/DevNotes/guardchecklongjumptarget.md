---
UID: ''
title: GuardCheckLongJumpTarget función)
description: Intenta comprobar si el destino de un longjmp es válido.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105656323"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="70dab-103">GuardCheckLongJumpTarget función)</span><span class="sxs-lookup"><span data-stu-id="70dab-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="70dab-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="70dab-104">Description</span></span>

<span data-ttu-id="70dab-105">Intenta comprobar si el destino de un [longjmp](/cpp/c-runtime-library/reference/longjmp) es válido para un proceso que tiene habilitada la [protección de flujo de control (cfg)](../secbp/control-flow-guard.md) .</span><span class="sxs-lookup"><span data-stu-id="70dab-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="70dab-106">Si la dirección de destino corresponde a una asignación de imagen, se extraen los destinos válidos para el archivo binario.</span><span class="sxs-lookup"><span data-stu-id="70dab-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="70dab-107">La función utiliza esos destinos para validar el destino.</span><span class="sxs-lookup"><span data-stu-id="70dab-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="70dab-108">Si el binario no tiene metadatos que describan el conjunto de destinos *longjmp* válidos, la función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="70dab-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="70dab-109">Si la dirección de destino corresponde a una asignación que no es de imagen, como en el código JIT, se consulta una directiva global de solo lectura para determinar si se permite el salto.</span><span class="sxs-lookup"><span data-stu-id="70dab-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="70dab-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70dab-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="70dab-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="70dab-111">TargetAddress [in]</span></span>

<span data-ttu-id="70dab-112">Dirección de destino del salto.</span><span class="sxs-lookup"><span data-stu-id="70dab-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="70dab-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="70dab-113">Flags [in]</span></span>

<span data-ttu-id="70dab-114">Marcas que describen la operación que se va a realizar en la dirección.</span><span class="sxs-lookup"><span data-stu-id="70dab-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="70dab-115">Si especifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), esta función no finaliza el proceso si el destino no es válido.</span><span class="sxs-lookup"><span data-stu-id="70dab-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="70dab-116">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="70dab-116">Returns</span></span>

<span data-ttu-id="70dab-117">**True** si el destino es válido; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="70dab-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70dab-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70dab-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="70dab-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="70dab-119">See also</span></span>
