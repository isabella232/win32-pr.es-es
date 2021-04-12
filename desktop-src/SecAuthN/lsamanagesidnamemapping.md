---
UID: ''
title: LsaManageSidNameMapping función)
description: Agrega o quita asignaciones de SID/nombre del conjunto de asignaciones registrado con el servicio de búsqueda de LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/22/2020
ms.locfileid: "104358759"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="ff64e-103">LsaManageSidNameMapping función)</span><span class="sxs-lookup"><span data-stu-id="ff64e-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="ff64e-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff64e-104">Description</span></span>

<span data-ttu-id="ff64e-105">La función **LsaManageSidNameMapping** agrega o quita asignaciones SID/Name del conjunto de asignaciones registrado con el servicio de búsqueda de LSA.</span><span class="sxs-lookup"><span data-stu-id="ff64e-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="ff64e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff64e-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="ff64e-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="ff64e-107">OpType [in]</span></span>

<span data-ttu-id="ff64e-108">Indica si se llama a esta función para agregar o quitar una asignación de SID/nombre.</span><span class="sxs-lookup"><span data-stu-id="ff64e-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="ff64e-109">OpInput [in]</span><span class="sxs-lookup"><span data-stu-id="ff64e-109">OpInput [in]</span></span>

<span data-ttu-id="ff64e-110">Indica los valores de dominio, cuenta y SID que se van a usar durante esta operación.</span><span class="sxs-lookup"><span data-stu-id="ff64e-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="ff64e-111">También se pueden establecer marcas adicionales en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ff64e-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="ff64e-112">OpOutput [out]</span><span class="sxs-lookup"><span data-stu-id="ff64e-112">OpOutput [out]</span></span>

<span data-ttu-id="ff64e-113">Contiene un valor de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) que indica si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="ff64e-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="ff64e-114">Value</span><span class="sxs-lookup"><span data-stu-id="ff64e-114">Value</span></span> | <span data-ttu-id="ff64e-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ff64e-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="ff64e-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="ff64e-116">**Success**</span></span> | <span data-ttu-id="ff64e-117">La operación se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="ff64e-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="ff64e-118">**NonMappingError**</span><span class="sxs-lookup"><span data-stu-id="ff64e-118">**NonMappingError**</span></span> | <span data-ttu-id="ff64e-119">Se ha producido un error no relacionado con la asignación de nombre de SID.</span><span class="sxs-lookup"><span data-stu-id="ff64e-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="ff64e-120">**NameCollision**</span><span class="sxs-lookup"><span data-stu-id="ff64e-120">**NameCollision**</span></span> | <span data-ttu-id="ff64e-121">Error de la operación debido a un conflicto de nombres.</span><span class="sxs-lookup"><span data-stu-id="ff64e-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="ff64e-122">**SidCollision**</span><span class="sxs-lookup"><span data-stu-id="ff64e-122">**SidCollision**</span></span> | <span data-ttu-id="ff64e-123">Error de la operación debido a un conflicto de SID.</span><span class="sxs-lookup"><span data-stu-id="ff64e-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="ff64e-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="ff64e-124">**DomainNotFound**</span></span> | <span data-ttu-id="ff64e-125">No se encontró el dominio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff64e-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="ff64e-126">**DomainSidPrefixMismatch**</span><span class="sxs-lookup"><span data-stu-id="ff64e-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="ff64e-127">El SID proporcionado no tiene el prefijo de dominio correcto.</span><span class="sxs-lookup"><span data-stu-id="ff64e-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="ff64e-128">**MappingNotFound**</span><span class="sxs-lookup"><span data-stu-id="ff64e-128">**MappingNotFound**</span></span> | <span data-ttu-id="ff64e-129">No se encontró la asignación en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="ff64e-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="ff64e-130">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="ff64e-130">Returns</span></span>

<span data-ttu-id="ff64e-131">Si la asignación se inserta correctamente, el valor devuelto es STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ff64e-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="ff64e-132">De lo contrario, si se produce un error en la función debido a conflictos de SID o de nombre, se devolverá STATUS_INVALID_PARAMETER error.</span><span class="sxs-lookup"><span data-stu-id="ff64e-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff64e-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff64e-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="ff64e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff64e-134">See also</span></span>
