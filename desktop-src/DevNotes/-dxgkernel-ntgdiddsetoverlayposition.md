---
description: Establece la posición de una superposición.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Función NtGdiDdSetOverlayPosition (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080113"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="9d3d5-103">NtGdiDdSetOverlayPosition función)</span><span class="sxs-lookup"><span data-stu-id="9d3d5-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="9d3d5-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9d3d5-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="9d3d5-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9d3d5-106">Establece la posición de una superposición.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d3d5-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="9d3d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d3d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3d5-109">*hSurfaceSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d3d5-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3d5-110">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que representa la superficie superpuesta de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="9d3d5-111">*hSurfaceDestination* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d3d5-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3d5-112">Puntero a una [**estructura \_ \_ local de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa la superficie que se está superpuesto.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="9d3d5-113">*puSetOverlayPositionData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9d3d5-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d3d5-114">Puntero a una estructura [**DD \_ SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) que contiene la información necesaria para establecer la posición de la superposición.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3d5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d3d5-115">Return value</span></span>

<span data-ttu-id="9d3d5-116">**NtGdiDdSetOverlayPosition** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9d3d5-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9d3d5-117">Return code</span></span>                                                                                              | <span data-ttu-id="9d3d5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d3d5-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d3d5-119"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="9d3d5-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9d3d5-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9d3d5-121">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9d3d5-122">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9d3d5-123"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d3d5-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9d3d5-124">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9d3d5-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9d3d5-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d3d5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d3d5-127">Requirements</span></span>



| <span data-ttu-id="9d3d5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d3d5-128">Requirement</span></span> | <span data-ttu-id="9d3d5-129">Value</span><span class="sxs-lookup"><span data-stu-id="9d3d5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3d5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d3d5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9d3d5-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d3d5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9d3d5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d3d5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9d3d5-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d3d5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9d3d5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d3d5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d3d5-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d3d5-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d3d5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d3d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3d5-137">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="9d3d5-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
