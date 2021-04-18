---
description: Extrae la información de encabezado de un delta.
title: ExtractPatchHeaderToFileA/W (función)
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721595"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="8bb2a-103">ExtractPatchHeaderToFileA/W (función)</span><span class="sxs-lookup"><span data-stu-id="8bb2a-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="8bb2a-104">Las funciones **ExtractPatchHeaderToFileA** y **ExtractPatchHeaderToFileW** extraen la información de encabezado de un delta.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="8bb2a-105">La diferencia se proporciona como una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-105">The delta is provided as a file path.</span></span> <span data-ttu-id="8bb2a-106">El encabezado de salida también se escribe en una ruta de acceso proporcionada.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb2a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bb2a-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="8bb2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bb2a-108">Parameters</span></span>

<span data-ttu-id="8bb2a-109">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="8bb2a-109">*PatchFileName*</span></span>

<span data-ttu-id="8bb2a-110">Nombre del delta que contiene el encabezado.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="8bb2a-111">*PatchHeaderFileName*</span><span class="sxs-lookup"><span data-stu-id="8bb2a-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="8bb2a-112">Nombre del archivo de encabezado que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bb2a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bb2a-113">Return value</span></span>

<span data-ttu-id="8bb2a-114">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="8bb2a-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb2a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb2a-115">Requirements</span></span>

| <span data-ttu-id="8bb2a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb2a-116">Requirement</span></span> | <span data-ttu-id="8bb2a-117">Value</span><span class="sxs-lookup"><span data-stu-id="8bb2a-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb2a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bb2a-118">Header</span></span> | <span data-ttu-id="8bb2a-119">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="8bb2a-119">patchapi.h</span></span> |
| <span data-ttu-id="8bb2a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bb2a-120">DLL</span></span> | <span data-ttu-id="8bb2a-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="8bb2a-121">mspatchc.dll</span></span> |
| <span data-ttu-id="8bb2a-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="8bb2a-122">Unicode</span></span> | <span data-ttu-id="8bb2a-123">Se implementa como ExtractPatchHeaderToFileW (Unicode) y ExtractPatchHeaderToFileA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8bb2a-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8bb2a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb2a-124">See also</span></span>

[<span data-ttu-id="8bb2a-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="8bb2a-125">PatchAPI</span></span>](patchapi.md)
