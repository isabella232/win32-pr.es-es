---
description: Usa la diferencia y el origen (proporcionados como búferes) para crear una nueva copia de los datos de destino. Los datos de salida se devuelven en un búfer asignado por MSDelta.
title: Función ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721601"
---
# <a name="applydeltab-function"></a><span data-ttu-id="03b6d-104">Función ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="03b6d-104">ApplyDeltaB function</span></span>

<span data-ttu-id="03b6d-105">Usa la diferencia y el origen (proporcionados como búferes) para crear una nueva copia de los datos de destino.</span><span class="sxs-lookup"><span data-stu-id="03b6d-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="03b6d-106">Los datos de salida se devuelven en un búfer asignado por MSDelta.</span><span class="sxs-lookup"><span data-stu-id="03b6d-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="03b6d-107">Debe llamar a [DeltaFree](msdelta-deltafree.md) para liberar el búfer de salida después de que esta función se haya completado.</span><span class="sxs-lookup"><span data-stu-id="03b6d-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="03b6d-108">Si el Delta especificado se creó con [PatchAPI](patchapi.md)y se establece la marca [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , MSDelta llamará a PatchAPI para aplicar la diferencia.</span><span class="sxs-lookup"><span data-stu-id="03b6d-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b6d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03b6d-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="03b6d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03b6d-110">Parameters</span></span>

<span data-ttu-id="03b6d-111">*ApplyFlags*</span><span class="sxs-lookup"><span data-stu-id="03b6d-111">*ApplyFlags*</span></span>

<span data-ttu-id="03b6d-112">de [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="03b6d-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="03b6d-113">*Origen*</span><span class="sxs-lookup"><span data-stu-id="03b6d-113">*Source*</span></span>

<span data-ttu-id="03b6d-114">de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="03b6d-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="03b6d-115">*Delta*</span><span class="sxs-lookup"><span data-stu-id="03b6d-115">*Delta*</span></span>

<span data-ttu-id="03b6d-116">de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos Delta.</span><span class="sxs-lookup"><span data-stu-id="03b6d-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="03b6d-117">*lpTarget*</span><span class="sxs-lookup"><span data-stu-id="03b6d-117">*lpTarget*</span></span>

<span data-ttu-id="03b6d-118">enuncia Puntero a la estructura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) en la que se va a escribir el destino.</span><span class="sxs-lookup"><span data-stu-id="03b6d-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="03b6d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03b6d-119">Return value</span></span>

<span data-ttu-id="03b6d-120">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="03b6d-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="03b6d-121">Cuando la función devuelve **false**, puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.</span><span class="sxs-lookup"><span data-stu-id="03b6d-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b6d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03b6d-122">Requirements</span></span>

| <span data-ttu-id="03b6d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b6d-123">Requirement</span></span> | <span data-ttu-id="03b6d-124">Value</span><span class="sxs-lookup"><span data-stu-id="03b6d-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03b6d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03b6d-125">Header</span></span> | <span data-ttu-id="03b6d-126">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="03b6d-126">msdelta.h</span></span> |
| <span data-ttu-id="03b6d-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03b6d-127">DLL</span></span> | <span data-ttu-id="03b6d-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="03b6d-128">msdelta.dll</span></span> |
| <span data-ttu-id="03b6d-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="03b6d-129">Unicode</span></span> | <span data-ttu-id="03b6d-130">No aplicable</span><span class="sxs-lookup"><span data-stu-id="03b6d-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="03b6d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="03b6d-131">See also</span></span>

[<span data-ttu-id="03b6d-132">MSDelta</span><span class="sxs-lookup"><span data-stu-id="03b6d-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="03b6d-133">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="03b6d-133">DeltaFree</span></span>](msdelta-deltafree.md)
