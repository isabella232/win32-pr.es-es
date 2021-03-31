---
description: Crea un contexto de dispositivo (DC) para la superficie especificada.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Función NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153080"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="8e349-103">NtGdiDdGetDC función)</span><span class="sxs-lookup"><span data-stu-id="8e349-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="8e349-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e349-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8e349-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="8e349-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8e349-106">Crea un contexto de dispositivo (DC) para la superficie especificada.</span><span class="sxs-lookup"><span data-stu-id="8e349-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e349-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e349-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="8e349-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e349-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e349-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e349-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e349-110">Identificador de una superficie de DirectDraw en modo kernel previamente devuelta por [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span><span class="sxs-lookup"><span data-stu-id="8e349-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e349-111">*puColorTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e349-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e349-112">Puntero a una tabla de colores de invalidación para el controlador de dominio devuelto.</span><span class="sxs-lookup"><span data-stu-id="8e349-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e349-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e349-113">Return value</span></span>

<span data-ttu-id="8e349-114">Si se realiza correctamente, esta función devuelve una **HDC**; válida. en caso contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="8e349-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e349-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e349-115">Remarks</span></span>

<span data-ttu-id="8e349-116">Solo se permite un DC por superficie en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="8e349-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="8e349-117">Las llamadas posteriores a **NtGdiDdGetDC** producirán un error hasta que se libere el controlador de dominio anterior.</span><span class="sxs-lookup"><span data-stu-id="8e349-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="8e349-118">Se recomienda que las aplicaciones llamen a [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) en su lugar, lo que proporciona la misma funcionalidad de una manera independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e349-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e349-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e349-119">Requirements</span></span>



| <span data-ttu-id="8e349-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e349-120">Requirement</span></span> | <span data-ttu-id="8e349-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e349-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e349-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e349-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e349-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8e349-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8e349-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e349-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e349-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8e349-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e349-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e349-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e349-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e349-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e349-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e349-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e349-129">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="8e349-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="8e349-130">**DdGetDC**</span><span class="sxs-lookup"><span data-stu-id="8e349-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
