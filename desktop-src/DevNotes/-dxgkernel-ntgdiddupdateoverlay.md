---
description: Cambia de posición o modifica los atributos visuales de una superficie superpuesta.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Función NtGdiDdUpdateOverlay (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998109"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="25210-103">NtGdiDdUpdateOverlay función)</span><span class="sxs-lookup"><span data-stu-id="25210-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="25210-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="25210-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="25210-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="25210-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="25210-106">Cambia de posición o modifica los atributos visuales de una superficie superpuesta.</span><span class="sxs-lookup"><span data-stu-id="25210-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="25210-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25210-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="25210-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25210-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25210-109">*hSurfaceDestination* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25210-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25210-110">Identificador del objeto DirectDraw en modo kernel creado previamente.</span><span class="sxs-lookup"><span data-stu-id="25210-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="25210-111">*hSurfaceSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25210-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25210-112">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie de superposición.</span><span class="sxs-lookup"><span data-stu-id="25210-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="25210-113">*puUpdateOverlayData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25210-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25210-114">Puntero a una estructura [**DD \_ UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) que contiene la información necesaria para actualizar la superposición.</span><span class="sxs-lookup"><span data-stu-id="25210-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25210-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25210-115">Return value</span></span>

<span data-ttu-id="25210-116">**NtGdiDdUpdateOverlay** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="25210-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="25210-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25210-117">Return code</span></span>                                                                                              | <span data-ttu-id="25210-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="25210-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25210-119"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="25210-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="25210-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="25210-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="25210-121">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="25210-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="25210-122">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="25210-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="25210-123"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25210-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="25210-124">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="25210-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="25210-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="25210-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="25210-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25210-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25210-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25210-127">Requirements</span></span>



| <span data-ttu-id="25210-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="25210-128">Requirement</span></span> | <span data-ttu-id="25210-129">Value</span><span class="sxs-lookup"><span data-stu-id="25210-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25210-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25210-130">Minimum supported client</span></span><br/> | <span data-ttu-id="25210-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25210-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="25210-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25210-132">Minimum supported server</span></span><br/> | <span data-ttu-id="25210-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25210-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25210-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25210-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="25210-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25210-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25210-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="25210-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25210-137">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="25210-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
