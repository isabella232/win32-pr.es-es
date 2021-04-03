---
description: Se usa para crear un comando de nivel de controlador o un búfer de vértice de la descripción especificada.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Función NtGdiDdCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998113"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="18f98-103">NtGdiDdCreateD3DBuffer función)</span><span class="sxs-lookup"><span data-stu-id="18f98-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="18f98-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="18f98-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="18f98-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="18f98-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="18f98-106">Se usa para crear un comando de nivel de controlador o un búfer de vértice de la descripción especificada.</span><span class="sxs-lookup"><span data-stu-id="18f98-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18f98-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="18f98-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18f98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f98-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18f98-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-110">Identificador de la [**estructura \_ \_ global DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el controlador.</span><span class="sxs-lookup"><span data-stu-id="18f98-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-111">*hSurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-112">Puntero a una matriz de identificadores de superficie.</span><span class="sxs-lookup"><span data-stu-id="18f98-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="18f98-113">El autor de la llamada puede establecer estos identificadores en los valores de identificador anteriores si se vuelven a crear las superficies después de un modificador de modo.</span><span class="sxs-lookup"><span data-stu-id="18f98-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="18f98-114">Este proceso se denomina "restaurar" en la documentación de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="18f98-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-115">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-116">Puntero a una estructura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que describe la superficie o el búfer que debe crear el controlador.</span><span class="sxs-lookup"><span data-stu-id="18f98-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-117">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-118">Puntero a una [**estructura \_ \_ global**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) de la superficie de tipo dd que contiene datos de superficie que se comparten globalmente con varias superficies.</span><span class="sxs-lookup"><span data-stu-id="18f98-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-119">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-120">Puntero a una lista de [**estructuras \_ \_ locales de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describen los objetos Surface creados por el controlador.</span><span class="sxs-lookup"><span data-stu-id="18f98-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="18f98-121">Normalmente solo hay una entrada en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="18f98-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-122">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-123">Puntero a una [**superficie de DD \_ \_ más**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estructura que contiene datos adicionales de la superficie local.</span><span class="sxs-lookup"><span data-stu-id="18f98-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-124">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-125">Puntero a una estructura [**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contiene la información necesaria para crear el búfer.</span><span class="sxs-lookup"><span data-stu-id="18f98-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="18f98-126">*puhSurface* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18f98-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f98-127">La API de DirectDraw usa y no debe rellenar el controlador.</span><span class="sxs-lookup"><span data-stu-id="18f98-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f98-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18f98-128">Return value</span></span>

<span data-ttu-id="18f98-129">**NtGdiDdCreateD3DBuffer** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="18f98-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="18f98-130">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="18f98-130">Return code</span></span>                                                                                              | <span data-ttu-id="18f98-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="18f98-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18f98-132"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="18f98-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="18f98-133">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="18f98-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="18f98-134">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="18f98-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="18f98-135">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="18f98-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="18f98-136"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18f98-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="18f98-137">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="18f98-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="18f98-138">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="18f98-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="18f98-139">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="18f98-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18f98-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18f98-140">Requirements</span></span>



| <span data-ttu-id="18f98-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="18f98-141">Requirement</span></span> | <span data-ttu-id="18f98-142">Value</span><span class="sxs-lookup"><span data-stu-id="18f98-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18f98-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18f98-143">Minimum supported client</span></span><br/> | <span data-ttu-id="18f98-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="18f98-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="18f98-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18f98-145">Minimum supported server</span></span><br/> | <span data-ttu-id="18f98-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18f98-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18f98-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18f98-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f98-148"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18f98-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f98-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="18f98-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f98-150">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="18f98-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
