---
description: Vacía la caché de compatibilidad de aplicaciones.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152900"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="e419a-103">BaseFlushAppcompatCache función)</span><span class="sxs-lookup"><span data-stu-id="e419a-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="e419a-104">Vacía la caché de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e419a-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="e419a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e419a-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="e419a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e419a-106">Parameters</span></span>

<span data-ttu-id="e419a-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e419a-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e419a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e419a-108">Return value</span></span>

<span data-ttu-id="e419a-109">La función devuelve **true** si se realiza correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e419a-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e419a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e419a-110">Remarks</span></span>

<span data-ttu-id="e419a-111">El autor de la llamada debe ser un administrador.</span><span class="sxs-lookup"><span data-stu-id="e419a-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="e419a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e419a-112">Requirements</span></span>



| <span data-ttu-id="e419a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e419a-113">Requirement</span></span> | <span data-ttu-id="e419a-114">Value</span><span class="sxs-lookup"><span data-stu-id="e419a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e419a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e419a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e419a-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e419a-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e419a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e419a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e419a-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e419a-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e419a-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e419a-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e419a-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e419a-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e419a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e419a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e419a-122">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="e419a-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




