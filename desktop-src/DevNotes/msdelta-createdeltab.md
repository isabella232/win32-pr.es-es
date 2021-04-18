---
description: Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve el delta de salida como un búfer asignado por MSDelta.
title: Función CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721577"
---
# <a name="createdeltab-function"></a><span data-ttu-id="30d3b-103">Función CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="30d3b-103">CreateDeltaB function</span></span>

<span data-ttu-id="30d3b-104">Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve el delta de salida como un búfer asignado por MSDelta.</span><span class="sxs-lookup"><span data-stu-id="30d3b-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="30d3b-105">Debe llamar a [DeltaFree](msdelta-deltafree.md) para liberar el búfer de salida después de que esta función se haya completado.</span><span class="sxs-lookup"><span data-stu-id="30d3b-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d3b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30d3b-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="30d3b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30d3b-107">Parameters</span></span>

<span data-ttu-id="30d3b-108">*FileTypeSet*</span><span class="sxs-lookup"><span data-stu-id="30d3b-108">*FileTypeSet*</span></span>

<span data-ttu-id="30d3b-109">de El valor de [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) que indica el tipo de archivo que se va a utilizar para el proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="30d3b-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="30d3b-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="30d3b-110">*SetFlags*</span></span>

<span data-ttu-id="30d3b-111">de Uno o más valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas que se van a utilizar durante el proceso de creación, además de las marcas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="30d3b-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="30d3b-112">*ResetFlags*</span><span class="sxs-lookup"><span data-stu-id="30d3b-112">*ResetFlags*</span></span>

<span data-ttu-id="30d3b-113">de Uno o más valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas predeterminadas que se restablecerán durante el proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="30d3b-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="30d3b-114">*Origen*</span><span class="sxs-lookup"><span data-stu-id="30d3b-114">*Source*</span></span>

<span data-ttu-id="30d3b-115">de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="30d3b-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="30d3b-116">*Target*</span><span class="sxs-lookup"><span data-stu-id="30d3b-116">*Target*</span></span>

<span data-ttu-id="30d3b-117">de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de destino.</span><span class="sxs-lookup"><span data-stu-id="30d3b-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="30d3b-118">*SourceOptions*</span><span class="sxs-lookup"><span data-stu-id="30d3b-118">*SourceOptions*</span></span>

<span data-ttu-id="30d3b-119">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="30d3b-119">[in] Reserved.</span></span> <span data-ttu-id="30d3b-120">Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con el valor *editable* establecido en **false**, *lpStart* establecido en **null** y *uSize* establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="30d3b-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="30d3b-121">*TargetOptions*</span><span class="sxs-lookup"><span data-stu-id="30d3b-121">*TargetOptions*</span></span>

<span data-ttu-id="30d3b-122">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="30d3b-122">[in] Reserved.</span></span> <span data-ttu-id="30d3b-123">Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con el valor *editable* establecido en **false**, *lpStart* establecido en **null** y *uSize* establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="30d3b-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="30d3b-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="30d3b-124">*GlobalOptions*</span></span>

<span data-ttu-id="30d3b-125">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="30d3b-125">[in] Reserved.</span></span> <span data-ttu-id="30d3b-126">Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *LpStart* establecido en **null** y *uSize* establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="30d3b-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="30d3b-127">*lpTargetFileTime*</span><span class="sxs-lookup"><span data-stu-id="30d3b-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="30d3b-128">de La marca de tiempo establecida en el archivo de destino después de aplicar la diferencia.</span><span class="sxs-lookup"><span data-stu-id="30d3b-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="30d3b-129">Si **es null**, la marca de tiempo de destino será la hora actual durante el proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="30d3b-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="30d3b-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="30d3b-130">*HashAlgId*</span></span>

<span data-ttu-id="30d3b-131">de ALG_ID del algoritmo que se va a utilizar para generar la firma de destino.</span><span class="sxs-lookup"><span data-stu-id="30d3b-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="30d3b-132">Algunos valores especiales son:</span><span class="sxs-lookup"><span data-stu-id="30d3b-132">Some special values are:</span></span>

- <span data-ttu-id="30d3b-133">0 = sin signatura</span><span class="sxs-lookup"><span data-stu-id="30d3b-133">0 = No signature</span></span>
- <span data-ttu-id="30d3b-134">32 = CRC de 32 bits definido en msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="30d3b-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="30d3b-135">*lpDelta*</span><span class="sxs-lookup"><span data-stu-id="30d3b-135">*lpDelta*</span></span>

<span data-ttu-id="30d3b-136">enuncia Puntero a la estructura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) en la que se va a escribir la diferencia.</span><span class="sxs-lookup"><span data-stu-id="30d3b-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="30d3b-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30d3b-137">Return value</span></span>

<span data-ttu-id="30d3b-138">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="30d3b-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="30d3b-139">Cuando la función devuelve **false**, puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.</span><span class="sxs-lookup"><span data-stu-id="30d3b-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d3b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30d3b-140">Requirements</span></span>

| <span data-ttu-id="30d3b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="30d3b-141">Requirement</span></span> | <span data-ttu-id="30d3b-142">Value</span><span class="sxs-lookup"><span data-stu-id="30d3b-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30d3b-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30d3b-143">Header</span></span> | <span data-ttu-id="30d3b-144">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="30d3b-144">msdelta.h</span></span> |
| <span data-ttu-id="30d3b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30d3b-145">DLL</span></span> | <span data-ttu-id="30d3b-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="30d3b-146">msdelta.dll</span></span> |
| <span data-ttu-id="30d3b-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="30d3b-147">Unicode</span></span> | <span data-ttu-id="30d3b-148">No aplicable</span><span class="sxs-lookup"><span data-stu-id="30d3b-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="30d3b-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="30d3b-149">See also</span></span>

[<span data-ttu-id="30d3b-150">MSDelta</span><span class="sxs-lookup"><span data-stu-id="30d3b-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="30d3b-151">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="30d3b-151">DeltaFree</span></span>](msdelta-deltafree.md)
