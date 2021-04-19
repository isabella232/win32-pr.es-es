---
description: Asocia una acción de prevención de pérdida de datos (DLP) de punto de conexión a un nivel de cumplimiento.
title: DLP_APP_OP_ENLIGHTENED_LEVEL estructura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495964"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="33d60-103">DLP_APP_OP_ENLIGHTENED_LEVEL estructura</span><span class="sxs-lookup"><span data-stu-id="33d60-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="33d60-104">Asocia una acción de prevención de pérdida de datos (DLP) de punto de conexión a un nivel de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="33d60-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33d60-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="33d60-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="33d60-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="33d60-107">*Operación* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="33d60-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33d60-108">Valor de la enumeración [DlpActionType](endpointdlp-dlpactiontype.md) que especifica el tipo de acción DLP del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="33d60-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="33d60-109">*AppEnforcementLevel* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="33d60-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33d60-110">Valor de [DlpAppEnforceLevel que](endpointdlp-dlpappenforcelevel.md) especifica el nivel de cumplimiento para el tipo de acción DLP de punto de conexión asociado.</span><span class="sxs-lookup"><span data-stu-id="33d60-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="33d60-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33d60-111">Remarks</span></span>

<span data-ttu-id="33d60-112">Pase una matriz de estas estructuras a [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) para establecer el modo de cumplimiento de un conjunto de operaciones DLP de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="33d60-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d60-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33d60-113">Requirements</span></span>



| <span data-ttu-id="33d60-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33d60-114">Requirement</span></span>          |    <span data-ttu-id="33d60-115">Value</span><span class="sxs-lookup"><span data-stu-id="33d60-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33d60-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33d60-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33d60-117">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="33d60-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

