---
description: Especifica el nivel de cumplimiento de una operación de prevención de pérdida de datos (DLP) del punto de conexión.
title: Enumeración DlpAppEnforceLevel (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495952"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="46df2-103">DlpAppEnforceLevel (enumeración)</span><span class="sxs-lookup"><span data-stu-id="46df2-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="46df2-104">Especifica el nivel de cumplimiento de una operación de prevención de pérdida de datos (DLP) del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="46df2-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46df2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46df2-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="46df2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="46df2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46df2-107">*DlpAppEnforceLevelNone* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="46df2-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46df2-108">Ninguna aplicación por parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46df2-108">No enforcement by the app.</span></span> <span data-ttu-id="46df2-109">El sistema DLP aplicará la operación.</span><span class="sxs-lookup"><span data-stu-id="46df2-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46df2-110">*DlpAppEnforceLevelNotify* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="46df2-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46df2-111">La aplicación Tne usará las API dlp para notificar al sistema DLP sobre la operación.</span><span class="sxs-lookup"><span data-stu-id="46df2-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="46df2-112">El sistema DLP aplicará la operación.</span><span class="sxs-lookup"><span data-stu-id="46df2-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46df2-113">*DlpAppEnforceLevelPrevent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="46df2-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46df2-114">No se admite en la versión actual.</span><span class="sxs-lookup"><span data-stu-id="46df2-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46df2-115">*DlpAppEnforceLevelFull* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="46df2-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46df2-116">No se admite en la versión actual.</span><span class="sxs-lookup"><span data-stu-id="46df2-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="46df2-117">*DlpAppEnforceLevelCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="46df2-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46df2-118">Valor máximo de la enumeración .</span><span class="sxs-lookup"><span data-stu-id="46df2-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="46df2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46df2-119">Remarks</span></span>

<span data-ttu-id="46df2-120">La estructura DLP_APP_OP_ENLIGHTENED_LEVEL utiliza [los valores de esta enumeración.](endpointdlp-dlp_app_op_enlightened_level.md)</span><span class="sxs-lookup"><span data-stu-id="46df2-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="46df2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46df2-121">Requirements</span></span>



| <span data-ttu-id="46df2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46df2-122">Requirement</span></span>          |    <span data-ttu-id="46df2-123">Value</span><span class="sxs-lookup"><span data-stu-id="46df2-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46df2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46df2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46df2-125">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="46df2-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

