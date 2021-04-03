---
description: Quita los datos adjuntos creados con NtGdiDdAttachSurface entre dos objetos de superficie de modo kernel.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Función NtGdiDdUnattachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998110"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="95d83-103">NtGdiDdUnattachSurface función)</span><span class="sxs-lookup"><span data-stu-id="95d83-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="95d83-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="95d83-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="95d83-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="95d83-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="95d83-106">Quita los datos adjuntos creados con [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)entre dos objetos de superficie de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="95d83-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d83-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95d83-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="95d83-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95d83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d83-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95d83-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d83-110">Objeto de superficie de modo kernel que se pasó como parámetro hSurfaceFrom a [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span><span class="sxs-lookup"><span data-stu-id="95d83-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d83-111">*hSurfaceAttached* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95d83-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d83-112">Objeto de superficie de modo kernel que se pasó como parámetro hSurfaceTo a [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d83-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95d83-113">Return value</span></span>

<span data-ttu-id="95d83-114">**NtGdiDdUnattachSurface** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="95d83-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="95d83-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="95d83-115">Return code</span></span>                                                                                              | <span data-ttu-id="95d83-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="95d83-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95d83-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="95d83-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="95d83-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="95d83-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="95d83-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="95d83-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="95d83-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="95d83-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="95d83-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95d83-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="95d83-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="95d83-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="95d83-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="95d83-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="95d83-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="95d83-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95d83-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95d83-125">Remarks</span></span>

<span data-ttu-id="95d83-126">Se recomienda que las aplicaciones usen la API de DirectDraw, que controla los datos adjuntos de la superficie de una manera de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="95d83-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="95d83-127">No es necesario llamar a esta función, ya que el kernel destruirá automáticamente todos los datos adjuntos cuando se llame a [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) .</span><span class="sxs-lookup"><span data-stu-id="95d83-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d83-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d83-128">Requirements</span></span>



| <span data-ttu-id="95d83-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d83-129">Requirement</span></span> | <span data-ttu-id="95d83-130">Value</span><span class="sxs-lookup"><span data-stu-id="95d83-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95d83-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d83-131">Minimum supported client</span></span><br/> | <span data-ttu-id="95d83-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95d83-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="95d83-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d83-133">Minimum supported server</span></span><br/> | <span data-ttu-id="95d83-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95d83-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95d83-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95d83-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d83-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d83-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d83-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d83-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d83-138">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="95d83-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




