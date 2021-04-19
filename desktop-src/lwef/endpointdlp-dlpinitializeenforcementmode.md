---
description: Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.
title: Función DlpInitializeEnforcementMode (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495919"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="4458a-103">Función DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="4458a-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="4458a-104">Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4458a-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4458a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4458a-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="4458a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4458a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4458a-107">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4458a-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4458a-108">DWORD **que** especifica el número de operaciones incluidas en la *matriz OperationEnforcement.*</span><span class="sxs-lookup"><span data-stu-id="4458a-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4458a-109">*OperationEnforcement* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4458a-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4458a-110">Matriz de estructuras [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) que especifican el nivel de cumplimiento de una operación DLP de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4458a-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="4458a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4458a-111">Return value</span></span>

<span data-ttu-id="4458a-112">Devuelve un valor HRESULT que incluye, entre otros, los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4458a-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="4458a-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4458a-113">HRESULT</span></span> | <span data-ttu-id="4458a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4458a-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="4458a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4458a-115">S_OK</span></span> | <span data-ttu-id="4458a-116">La función se completó correctamente</span><span class="sxs-lookup"><span data-stu-id="4458a-116">The function completed successfully</span></span> |
| <span data-ttu-id="4458a-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4458a-117">E_INVALIDARG</span></span> | <span data-ttu-id="4458a-118">Uno o varios de los parámetros de función no son válidos.</span><span class="sxs-lookup"><span data-stu-id="4458a-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="4458a-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4458a-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="4458a-120">Error de asignación de memoria para la operación.</span><span class="sxs-lookup"><span data-stu-id="4458a-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="4458a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4458a-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="4458a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4458a-122">Requirements</span></span>



| <span data-ttu-id="4458a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4458a-123">Requirement</span></span>          |    <span data-ttu-id="4458a-124">Value</span><span class="sxs-lookup"><span data-stu-id="4458a-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4458a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4458a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4458a-126">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="4458a-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="4458a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4458a-127">DLL</span></span><br/>                      | <span data-ttu-id="4458a-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="4458a-128">EndpointDlp.dll</span></span> |