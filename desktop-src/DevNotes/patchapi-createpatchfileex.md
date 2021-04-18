---
description: Crea una diferencia entre el archivo de código fuente especificado y el archivo de destino especificado.
title: CreatePatchFileExA/W (función)
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721575"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="6c336-103">CreatePatchFileExA/W (función)</span><span class="sxs-lookup"><span data-stu-id="6c336-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="6c336-104">Las funciones **CreatePatchFileExA** y **CreatePatchFileExW** crean una diferencia entre el archivo de código fuente especificado y el archivo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="6c336-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="6c336-105">Los archivos de origen y de destino se proporcionan como rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="6c336-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="6c336-106">El delta de salida también se escribe en una ruta de acceso proporcionada.</span><span class="sxs-lookup"><span data-stu-id="6c336-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="6c336-107">Estas funciones proporcionan informes de progreso durante el proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="6c336-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c336-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c336-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="6c336-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c336-109">Parameters</span></span>

<span data-ttu-id="6c336-110">*OldFileCount*</span><span class="sxs-lookup"><span data-stu-id="6c336-110">*OldFileCount*</span></span>

<span data-ttu-id="6c336-111">Número total de archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6c336-111">The total number of source files.</span></span> <span data-ttu-id="6c336-112">Se usa para crear diferencias en varios archivos de código fuente (255 como máximo).</span><span class="sxs-lookup"><span data-stu-id="6c336-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="6c336-113">*OldFileInfoArray*</span><span class="sxs-lookup"><span data-stu-id="6c336-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="6c336-114">Puntero a la matriz de información del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6c336-114">Pointer to source file information array.</span></span>

<span data-ttu-id="6c336-115">*NewFileName*</span><span class="sxs-lookup"><span data-stu-id="6c336-115">*NewFileName*</span></span>

<span data-ttu-id="6c336-116">Nombre del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6c336-116">The name of the target file.</span></span>

<span data-ttu-id="6c336-117">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="6c336-117">*PatchFileName*</span></span>

<span data-ttu-id="6c336-118">Nombre del delta que se crea.</span><span class="sxs-lookup"><span data-stu-id="6c336-118">The name of the delta that is created.</span></span>

<span data-ttu-id="6c336-119">*OptionFlags*</span><span class="sxs-lookup"><span data-stu-id="6c336-119">*OptionFlags*</span></span>

<span data-ttu-id="6c336-120">Marcas de creación.</span><span class="sxs-lookup"><span data-stu-id="6c336-120">Creation flags.</span></span>

<span data-ttu-id="6c336-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="6c336-121">*ProgressCallback*</span></span>

<span data-ttu-id="6c336-122">Puntero a una devolución de llamada de progreso definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c336-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="6c336-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="6c336-123">*CallbackContext*</span></span>

<span data-ttu-id="6c336-124">Puntero a un contexto definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c336-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c336-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c336-125">Return value</span></span>

<span data-ttu-id="6c336-126">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="6c336-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c336-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c336-127">Requirements</span></span>

| <span data-ttu-id="6c336-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c336-128">Requirement</span></span> | <span data-ttu-id="6c336-129">Value</span><span class="sxs-lookup"><span data-stu-id="6c336-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c336-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c336-130">Header</span></span> | <span data-ttu-id="6c336-131">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="6c336-131">patchapi.h</span></span> |
| <span data-ttu-id="6c336-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c336-132">DLL</span></span> | <span data-ttu-id="6c336-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="6c336-133">mspatchc.dll</span></span> |
| <span data-ttu-id="6c336-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="6c336-134">Unicode</span></span> | <span data-ttu-id="6c336-135">Se implementa como CreatePatchFileExW (Unicode) y CreatePatchFileExA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c336-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="6c336-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c336-136">See also</span></span>

[<span data-ttu-id="6c336-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="6c336-137">PatchAPI</span></span>](patchapi.md)
