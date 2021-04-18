---
description: Libera el bloque de memoria especificado.
title: Función DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721599"
---
# <a name="deltafree-function"></a><span data-ttu-id="89bc2-103">Función DeltaFree</span><span class="sxs-lookup"><span data-stu-id="89bc2-103">DeltaFree function</span></span>

<span data-ttu-id="89bc2-104">Libera el bloque de memoria especificado.</span><span class="sxs-lookup"><span data-stu-id="89bc2-104">Frees the specified memory block.</span></span> <span data-ttu-id="89bc2-105">Debe llamar a esta función después de las llamadas correctas a [CreateDeltaB](msdelta-createdeltab.md) y [ApplyDeltaB](msdelta-applydeltab.md) para liberar el búfer de memoria asignado a MSDelta.</span><span class="sxs-lookup"><span data-stu-id="89bc2-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="89bc2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89bc2-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="89bc2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89bc2-107">Parameters</span></span>

<span data-ttu-id="89bc2-108">*lpMemory*</span><span class="sxs-lookup"><span data-stu-id="89bc2-108">*lpMemory*</span></span>

<span data-ttu-id="89bc2-109">de Bloque de memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="89bc2-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="89bc2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89bc2-110">Return value</span></span>

<span data-ttu-id="89bc2-111">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="89bc2-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="89bc2-112">Cuando la función devuelve **false**, puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.</span><span class="sxs-lookup"><span data-stu-id="89bc2-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89bc2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89bc2-113">Requirements</span></span>

| <span data-ttu-id="89bc2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89bc2-114">Requirement</span></span> | <span data-ttu-id="89bc2-115">Value</span><span class="sxs-lookup"><span data-stu-id="89bc2-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89bc2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89bc2-116">Header</span></span> | <span data-ttu-id="89bc2-117">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="89bc2-117">msdelta.h</span></span> |
| <span data-ttu-id="89bc2-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89bc2-118">DLL</span></span> | <span data-ttu-id="89bc2-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="89bc2-119">msdelta.dll</span></span> |
| <span data-ttu-id="89bc2-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="89bc2-120">Unicode</span></span> | <span data-ttu-id="89bc2-121">No aplicable</span><span class="sxs-lookup"><span data-stu-id="89bc2-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="89bc2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="89bc2-122">See also</span></span>

[<span data-ttu-id="89bc2-123">MSDelta</span><span class="sxs-lookup"><span data-stu-id="89bc2-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="89bc2-124">CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="89bc2-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="89bc2-125">ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="89bc2-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
