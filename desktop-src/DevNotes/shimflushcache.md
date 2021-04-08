---
description: Vacía la caché de la base de datos de correcciones de compatibilidad. Se debe llamar a esta función después de instalar una nueva base de datos de correcciones de compatibilidad.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080086"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="3cdfc-104">ShimFlushCache función)</span><span class="sxs-lookup"><span data-stu-id="3cdfc-104">ShimFlushCache function</span></span>

<span data-ttu-id="3cdfc-105">Vacía la caché de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-105">Flushes the shim database cache.</span></span> <span data-ttu-id="3cdfc-106">Se debe llamar a esta función después de instalar una nueva base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdfc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cdfc-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="3cdfc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cdfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cdfc-109">*hWnd* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfc-110">Sin usar debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfc-111">*hInstance* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfc-112">Sin usar debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfc-113">*lpszCmdLine* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfc-114">Sin usar debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfc-115">*nCmdShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfc-116">Sin usar debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cdfc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cdfc-117">Return value</span></span>

<span data-ttu-id="3cdfc-118">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cdfc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cdfc-119">Remarks</span></span>

<span data-ttu-id="3cdfc-120">El autor de la llamada debe ser un administrador.</span><span class="sxs-lookup"><span data-stu-id="3cdfc-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cdfc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cdfc-121">Requirements</span></span>



| <span data-ttu-id="3cdfc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cdfc-122">Requirement</span></span> | <span data-ttu-id="3cdfc-123">Value</span><span class="sxs-lookup"><span data-stu-id="3cdfc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdfc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cdfc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3cdfc-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3cdfc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cdfc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3cdfc-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3cdfc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3cdfc-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3cdfc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cdfc-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cdfc-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cdfc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cdfc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cdfc-131">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="3cdfc-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




