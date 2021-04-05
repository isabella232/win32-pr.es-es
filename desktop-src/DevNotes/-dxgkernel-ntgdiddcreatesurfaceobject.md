---
description: Crea un objeto de superficie de modo kernel que representa el objeto de superficie de modo de usuario al que hace referencia puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Función NtGdiDdCreateSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080115"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="4e3d4-103">NtGdiDdCreateSurfaceObject función)</span><span class="sxs-lookup"><span data-stu-id="4e3d4-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="4e3d4-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4e3d4-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4e3d4-106">Crea un objeto de superficie de modo kernel que representa el objeto de superficie de modo de usuario al que hace referencia *puSurfaceLocal*.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e3d4-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="4e3d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e3d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3d4-109">*hDirectDrawLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-110">Identificador del objeto DirectDraw en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="4e3d4-111">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-112">Identificador anterior de la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-112">Previous handle to the same surface.</span></span> <span data-ttu-id="4e3d4-113">Se usa si la superficie se vuelve a crear después de un cambio de modo.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="4e3d4-114">*puSurfaceLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-115">Puntero a la [**estructura \_ \_ local del área DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa el objeto de superficie del modo de usuario de DirectDraw con el que se va a asociar la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="4e3d4-116">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e3d4-117">*puSurfaceMore* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-118">Puntero a la [**superficie de la DD \_ \_ más**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estructura que contiene datos locales adicionales para cada objeto de superficie individual.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="4e3d4-119">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e3d4-120">*puSurfaceGlobal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-121">Puntero a la [**estructura \_ \_ global**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) de la superficie de DD que contiene los datos de la superficie compartidos globalmente con varias superficies.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="4e3d4-122">Consulte la documentación de DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e3d4-123">*bComplete* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e3d4-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d4-124">Marca de finalización de objeto en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="4e3d4-125">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="4e3d4-126">REALES</span><span class="sxs-lookup"><span data-stu-id="4e3d4-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="4e3d4-127">Complete todo el procesamiento relacionado con la representación en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="4e3d4-128">ES</span><span class="sxs-lookup"><span data-stu-id="4e3d4-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="4e3d4-129">Cree el objeto, pero no configure datos internos, como el puntero de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="4e3d4-130">Los objetos creados con **false** se pueden adjuntar mediante [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) y se completan mediante una llamada a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span><span class="sxs-lookup"><span data-stu-id="4e3d4-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3d4-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e3d4-131">Return value</span></span>

<span data-ttu-id="4e3d4-132">Si se realiza correctamente, esta función devuelve un identificador a la representación de la superficie del modo kernel; en caso contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3d4-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e3d4-133">Remarks</span></span>

<span data-ttu-id="4e3d4-134">Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="4e3d4-135">Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e3d4-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3d4-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e3d4-136">Requirements</span></span>



| <span data-ttu-id="4e3d4-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e3d4-137">Requirement</span></span> | <span data-ttu-id="4e3d4-138">Value</span><span class="sxs-lookup"><span data-stu-id="4e3d4-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3d4-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e3d4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3d4-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4e3d4-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4e3d4-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e3d4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3d4-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e3d4-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4e3d4-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e3d4-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e3d4-144"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e3d4-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3d4-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e3d4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3d4-146">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="4e3d4-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="4e3d4-147">**DdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="4e3d4-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="4e3d4-148">**NtGdiDdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="4e3d4-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="4e3d4-149">**NtGdiDdAttachSurface**</span><span class="sxs-lookup"><span data-stu-id="4e3d4-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="4e3d4-150">**NtGdiDdCreateSurface**</span><span class="sxs-lookup"><span data-stu-id="4e3d4-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
