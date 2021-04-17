---
description: Devuelve el identificador de la API de Microsoft DirectX de modo kernel que se va a usar en las llamadas posteriores a los puntos de entrada de modo kernel que controlan el mecanismo de la API de DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Función NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659537"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="75160-103">NtGdiDdGetDxHandle función)</span><span class="sxs-lookup"><span data-stu-id="75160-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="75160-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="75160-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="75160-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="75160-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="75160-106">Devuelve el identificador de la API de Microsoft DirectX de modo kernel que se va a usar en las llamadas posteriores a los puntos de entrada de modo kernel que controlan el mecanismo de la API de DirectX.</span><span class="sxs-lookup"><span data-stu-id="75160-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="75160-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75160-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="75160-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75160-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75160-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75160-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75160-110">Identificador del objeto DirectDraw propietario de la superficie.</span><span class="sxs-lookup"><span data-stu-id="75160-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="75160-111">Este parámetro es opcional y se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="75160-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75160-112">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75160-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75160-113">Identificador de la superficie para la que se va a devolver un identificador de API de DirectX en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="75160-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="75160-114">Este parámetro es opcional y se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="75160-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75160-115">*bRelease* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75160-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75160-116">Establézcalo en **true** si se debe liberar la interfaz del modo kernel de la API de DirectX.</span><span class="sxs-lookup"><span data-stu-id="75160-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="75160-117">En caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="75160-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75160-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75160-118">Return value</span></span>

<span data-ttu-id="75160-119">Un identificador de API de DirectX que se usa en los siguientes puntos de entrada de kernel orientados a API de DirectX.</span><span class="sxs-lookup"><span data-stu-id="75160-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="75160-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75160-120">Remarks</span></span>

<span data-ttu-id="75160-121">Si se especifican *hDirectDraw* y *hSurface* , se omite *hSurface* .</span><span class="sxs-lookup"><span data-stu-id="75160-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="75160-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75160-122">Requirements</span></span>



| <span data-ttu-id="75160-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="75160-123">Requirement</span></span> | <span data-ttu-id="75160-124">Value</span><span class="sxs-lookup"><span data-stu-id="75160-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75160-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75160-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75160-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="75160-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="75160-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75160-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75160-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75160-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="75160-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75160-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="75160-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75160-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75160-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="75160-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75160-132">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="75160-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




