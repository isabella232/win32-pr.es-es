---
description: Recupera un identificador de objeto para el objeto especificado asociado al proceso especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Función ObFindHandleForObject (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907060"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="3a2f5-103">ObFindHandleForObject función)</span><span class="sxs-lookup"><span data-stu-id="3a2f5-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="3a2f5-104">\[Esta función está obsoleta y puede modificarse o no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="3a2f5-105">Evite el uso de esta función.\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-105">Avoid using this function.\]</span></span>

<span data-ttu-id="3a2f5-106">Recupera un identificador de objeto para el objeto especificado asociado al proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a2f5-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="3a2f5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a2f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2f5-109">*Proceso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2f5-110">Proceso.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-110">The process.</span></span> <span data-ttu-id="3a2f5-111">Este identificador es devuelto por la función **IoGetCurrentProcess** o **PsGetCurrentProcess** .</span><span class="sxs-lookup"><span data-stu-id="3a2f5-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="3a2f5-112">*Objeto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2f5-113">Puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="3a2f5-114">*Reserved1* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2f5-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3a2f5-116">*Reserved2* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2f5-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3a2f5-118">*Identificador* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2f5-119">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2f5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a2f5-120">Return value</span></span>

<span data-ttu-id="3a2f5-121">La función devuelve **true** si se encuentra una coincidencia y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2f5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a2f5-122">Remarks</span></span>

<span data-ttu-id="3a2f5-123">Esta función está disponible en Ntoskrnl.exe y solo se puede llamar desde el modo kernel.</span><span class="sxs-lookup"><span data-stu-id="3a2f5-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="3a2f5-124">La biblioteca de importación correspondiente está disponible a través de Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="3a2f5-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2f5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2f5-125">Requirements</span></span>



| <span data-ttu-id="3a2f5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2f5-126">Requirement</span></span> | <span data-ttu-id="3a2f5-127">Value</span><span class="sxs-lookup"><span data-stu-id="3a2f5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2f5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a2f5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2f5-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3a2f5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a2f5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2f5-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a2f5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a2f5-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a2f5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2f5-133"><dt>Ntosp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a2f5-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="3a2f5-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a2f5-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a2f5-135"><dt>Ntoskrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a2f5-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




