---
description: 'Función NtGdiDdAddAttachedSurface: adjunta una superficie a otra superficie.'
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Función NtGdiDdAddAttachedSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085793"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="0a106-103">Función NtGdiDdAddAttachedSurface</span><span class="sxs-lookup"><span data-stu-id="0a106-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="0a106-104">\[Esta función está sujeta a cambios con cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0a106-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0a106-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="0a106-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0a106-106">Adjunta una superficie a otra superficie.</span><span class="sxs-lookup"><span data-stu-id="0a106-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a106-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a106-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="0a106-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a106-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a106-109">*hSurface* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0a106-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a106-110">Identificador de una [**estructura LOCAL de DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa la superficie a la que se asocia otra superficie.</span><span class="sxs-lookup"><span data-stu-id="0a106-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="0a106-111">*hSurfaceAttached* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0a106-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a106-112">Identificador de una [**estructura LOCAL de DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa la superficie que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="0a106-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="0a106-113">*puAddAttachedSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0a106-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a106-114">Puntero a una [**estructura \_ ADDATTACHEDSURFACEDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) que contiene la información necesaria para que el controlador realice los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0a106-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a106-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a106-115">Return value</span></span>

<span data-ttu-id="0a106-116">**NtGdiDdAddAttachedSurface** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0a106-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="0a106-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0a106-117">Return code</span></span>                                                                                              | <span data-ttu-id="0a106-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a106-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a106-119"><dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt></span><span class="sxs-lookup"><span data-stu-id="0a106-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="0a106-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="0a106-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="0a106-121">Si este código es DD \_ correcto, DirectDraw o Direct3D continúa con la función .</span><span class="sxs-lookup"><span data-stu-id="0a106-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="0a106-122">De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.</span><span class="sxs-lookup"><span data-stu-id="0a106-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0a106-123"><dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt></span><span class="sxs-lookup"><span data-stu-id="0a106-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="0a106-124">El controlador no tiene ningún comentario sobre la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="0a106-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="0a106-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="0a106-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="0a106-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0a106-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a106-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a106-127">Requirements</span></span>



| <span data-ttu-id="0a106-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a106-128">Requirement</span></span> | <span data-ttu-id="0a106-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0a106-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a106-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a106-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0a106-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a106-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0a106-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a106-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0a106-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a106-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a106-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a106-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a106-135"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="0a106-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a106-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a106-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a106-137">Compatibilidad con clientes de bajo nivel de gráficos</span><span class="sxs-lookup"><span data-stu-id="0a106-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
