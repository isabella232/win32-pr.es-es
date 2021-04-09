---
description: Conecta una superficie a otra superficie.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Función NtGdiDdCreateSurface (Ntgdi. h)
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
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152811"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="bafdd-103">NtGdiDdCreateSurface función)</span><span class="sxs-lookup"><span data-stu-id="bafdd-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="bafdd-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bafdd-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bafdd-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bafdd-106">Conecta una superficie a otra superficie.</span><span class="sxs-lookup"><span data-stu-id="bafdd-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafdd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bafdd-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bafdd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bafdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bafdd-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-110">Identificador de la [**estructura \_ \_ global DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el controlador.</span><span class="sxs-lookup"><span data-stu-id="bafdd-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-111">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-112">Identificador anterior de la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="bafdd-112">Previous handle to the same surface.</span></span> <span data-ttu-id="bafdd-113">Se usa si la superficie se vuelve a crear después de un cambio de modo.</span><span class="sxs-lookup"><span data-stu-id="bafdd-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-114">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-115">Puntero a la estructura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que describe la superficie o el búfer que debe crear el controlador.</span><span class="sxs-lookup"><span data-stu-id="bafdd-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-116">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-117">Puntero a la [**estructura \_ \_ global de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contiene los datos de la superficie que se comparten globalmente con varias superficies.</span><span class="sxs-lookup"><span data-stu-id="bafdd-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-118">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-119">Puntero a una lista de [**estructuras \_ \_ locales de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describen los objetos Surface creados por el controlador.</span><span class="sxs-lookup"><span data-stu-id="bafdd-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-120">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-121">Puntero a una [**superficie de DD \_ \_ más**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estructura que contiene datos adicionales de la superficie local.</span><span class="sxs-lookup"><span data-stu-id="bafdd-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-122">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-123">Puntero a una estructura [**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contiene la información necesaria para crear una superficie.</span><span class="sxs-lookup"><span data-stu-id="bafdd-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="bafdd-124">*puhSurface* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bafdd-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bafdd-125">La API de DirectDraw usa y no debe rellenar el controlador.</span><span class="sxs-lookup"><span data-stu-id="bafdd-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bafdd-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bafdd-126">Return value</span></span>

<span data-ttu-id="bafdd-127">**NtGdiDdCreateSurface** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bafdd-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="bafdd-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bafdd-128">Return code</span></span>                                                                                              | <span data-ttu-id="bafdd-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="bafdd-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bafdd-130"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="bafdd-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="bafdd-131">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="bafdd-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="bafdd-132">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="bafdd-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="bafdd-133">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="bafdd-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="bafdd-134"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bafdd-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="bafdd-135">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bafdd-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="bafdd-136">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="bafdd-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="bafdd-137">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bafdd-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bafdd-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bafdd-138">Remarks</span></span>

<span data-ttu-id="bafdd-139">Se recomienda que la aplicación llame a [IDirectDraw7:: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) en lugar de usar esta función.</span><span class="sxs-lookup"><span data-stu-id="bafdd-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="bafdd-140">Al crear una cadena de superficies asociadas, como una cadena o cadena de intercambio, se debe llamar primero a [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) para cada superficie.</span><span class="sxs-lookup"><span data-stu-id="bafdd-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="bafdd-141">A continuación, llame a [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) para adjuntarlos.</span><span class="sxs-lookup"><span data-stu-id="bafdd-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="bafdd-142">Por último, llame a **NtGdiDdCreateSurface** solo para la primera superficie de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bafdd-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="bafdd-143">En este caso, *hSurface* sería el identificador devuelto por **NtGdiDdCreateSurfaceObject** para la primera superficie de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bafdd-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="bafdd-144">Solo se debe llamar a **NtGdiDdCreateSurface** para crear superficies en la memoria de vídeo local y no local.</span><span class="sxs-lookup"><span data-stu-id="bafdd-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="bafdd-145">Nunca se debe llamar para crear superficies de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="bafdd-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="bafdd-146">Para crear superficies de memoria del sistema, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bafdd-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="bafdd-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bafdd-147">Requirements</span></span>



| <span data-ttu-id="bafdd-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="bafdd-148">Requirement</span></span> | <span data-ttu-id="bafdd-149">Value</span><span class="sxs-lookup"><span data-stu-id="bafdd-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bafdd-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bafdd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bafdd-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bafdd-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bafdd-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bafdd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bafdd-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bafdd-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bafdd-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bafdd-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bafdd-155"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bafdd-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bafdd-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="bafdd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafdd-157">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="bafdd-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
