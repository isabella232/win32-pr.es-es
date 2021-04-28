---
description: 'Función NtGdiDdCreateSurface: adjunta una superficie a otra superficie.'
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Función NtGdiDdCreateSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085783"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="61636-103">Función NtGdiDdCreateSurface</span><span class="sxs-lookup"><span data-stu-id="61636-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="61636-104">\[Esta función está sujeta a cambios con cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61636-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="61636-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="61636-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="61636-106">Adjunta una superficie a otra superficie.</span><span class="sxs-lookup"><span data-stu-id="61636-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="61636-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61636-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="61636-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61636-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61636-109">*hDirectDraw* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="61636-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-110">Identificador de la [**estructura \_ DD DIRECTDRAW \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el controlador.</span><span class="sxs-lookup"><span data-stu-id="61636-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="61636-111">*hSurface* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="61636-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-112">Identificador anterior a la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="61636-112">Previous handle to the same surface.</span></span> <span data-ttu-id="61636-113">Se usa si la superficie se vuelve a crear después de un cambio de modo.</span><span class="sxs-lookup"><span data-stu-id="61636-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="61636-114">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61636-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-115">Puntero a la [**estructura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que describe la superficie o el búfer que debe crear el controlador.</span><span class="sxs-lookup"><span data-stu-id="61636-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="61636-116">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61636-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-117">Puntero a la [**estructura GLOBAL \_ de DD SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contiene datos de superficie que se comparten globalmente con varias superficies.</span><span class="sxs-lookup"><span data-stu-id="61636-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="61636-118">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61636-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-119">Puntero a una lista de estructuras [**\_ \_ LOCALES de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describen los objetos de superficie creados por el controlador.</span><span class="sxs-lookup"><span data-stu-id="61636-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="61636-120">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61636-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-121">Puntero a una [**estructura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) que contiene datos de superficie locales adicionales.</span><span class="sxs-lookup"><span data-stu-id="61636-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="61636-122">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61636-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-123">Puntero a una [**estructura \_ CREATESURFACEDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contiene la información necesaria para crear una superficie.</span><span class="sxs-lookup"><span data-stu-id="61636-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="61636-124">*puhSurface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61636-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61636-125">La API de DirectDraw la usa y el controlador no debe rellenarla.</span><span class="sxs-lookup"><span data-stu-id="61636-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61636-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61636-126">Return value</span></span>

<span data-ttu-id="61636-127">**NtGdiDdCreateSurface devuelve** uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="61636-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="61636-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="61636-128">Return code</span></span>                                                                                              | <span data-ttu-id="61636-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="61636-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61636-130"><dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt></span><span class="sxs-lookup"><span data-stu-id="61636-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="61636-131">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="61636-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="61636-132">Si este código es DD \_ correcto, DirectDraw o Direct3D continúa con la función .</span><span class="sxs-lookup"><span data-stu-id="61636-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="61636-133">De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.</span><span class="sxs-lookup"><span data-stu-id="61636-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="61636-134"><dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt></span><span class="sxs-lookup"><span data-stu-id="61636-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="61636-135">El controlador no tiene ningún comentario sobre la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="61636-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="61636-136">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="61636-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="61636-137">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="61636-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61636-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61636-138">Remarks</span></span>

<span data-ttu-id="61636-139">Se recomienda que la aplicación llame a [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) en lugar de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="61636-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="61636-140">Al crear una cadena de superficies adjuntas, como una cadena de intercambio o cadena o mapas mip, se debe llamar primero a [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) para cada superficie.</span><span class="sxs-lookup"><span data-stu-id="61636-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="61636-141">A continuación, llame a [**NtGdiDdAttachSurface para**](-dxgkernel-ntgdiddattachsurface.md) adjuntarlos.</span><span class="sxs-lookup"><span data-stu-id="61636-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="61636-142">Por último, llame **a NtGdiDdCreateSurface** solo para la primera superficie de la cadena.</span><span class="sxs-lookup"><span data-stu-id="61636-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="61636-143">En este caso, *hSurface sería el* identificador devuelto por **NtGdiDdCreateSurfaceObject** para la primera superficie de la cadena.</span><span class="sxs-lookup"><span data-stu-id="61636-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="61636-144">**Solo se debe llamar a NtGdiDdCreateSurface** para crear superficies en memoria de vídeo local y no local.</span><span class="sxs-lookup"><span data-stu-id="61636-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="61636-145">Nunca se debe llamar a para crear superficies de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="61636-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="61636-146">Para crear superficies de memoria del sistema, use [**NtGdiDdCreateSurfaceObject en su**](-dxgkernel-ntgdiddcreatesurfaceobject.md) lugar.</span><span class="sxs-lookup"><span data-stu-id="61636-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="61636-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61636-147">Requirements</span></span>



| <span data-ttu-id="61636-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="61636-148">Requirement</span></span> | <span data-ttu-id="61636-149">Valor</span><span class="sxs-lookup"><span data-stu-id="61636-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61636-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61636-150">Minimum supported client</span></span><br/> | <span data-ttu-id="61636-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="61636-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="61636-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61636-152">Minimum supported server</span></span><br/> | <span data-ttu-id="61636-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61636-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="61636-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61636-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="61636-155"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="61636-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61636-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61636-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61636-157">Compatibilidad con clientes de bajo nivel de gráficos</span><span class="sxs-lookup"><span data-stu-id="61636-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
