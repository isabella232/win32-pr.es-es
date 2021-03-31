---
description: Destruye un objeto Surface de Microsoft DirectDraw de modo kernel previamente asignado que se creó con el miembro dwCaps de la estructura DDSCAPS establecida en DDSCAPS \_ EXECUTEBUFFER.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: Función NtGdiDdDestroyD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806938"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="4623f-103">NtGdiDdDestroyD3DBuffer función)</span><span class="sxs-lookup"><span data-stu-id="4623f-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="4623f-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4623f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4623f-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="4623f-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4623f-106">Destruye un objeto Surface de Microsoft DirectDraw de modo kernel previamente asignado que se creó con el miembro **dwCaps** de la estructura [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) establecida en DDSCAPS \_ EXECUTEBUFFER.</span><span class="sxs-lookup"><span data-stu-id="4623f-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="4623f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4623f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="4623f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4623f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4623f-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4623f-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4623f-110">Identificador de una estructura de [**\_ DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) de datos de almacenamiento que contiene la información necesaria para destruir un comando Direct3D o un búfer de vértice.</span><span class="sxs-lookup"><span data-stu-id="4623f-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4623f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4623f-111">Return value</span></span>

<span data-ttu-id="4623f-112">**NtGdiDdDestroyD3DBuffer** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4623f-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="4623f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4623f-113">Return code</span></span>                                                                                              | <span data-ttu-id="4623f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4623f-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4623f-115"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="4623f-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="4623f-116">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="4623f-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="4623f-117">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="4623f-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="4623f-118">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="4623f-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4623f-119"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4623f-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="4623f-120">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="4623f-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="4623f-121">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="4623f-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="4623f-122">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4623f-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4623f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4623f-123">Requirements</span></span>



| <span data-ttu-id="4623f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4623f-124">Requirement</span></span> | <span data-ttu-id="4623f-125">Value</span><span class="sxs-lookup"><span data-stu-id="4623f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4623f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4623f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4623f-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4623f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4623f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4623f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4623f-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4623f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4623f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4623f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4623f-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4623f-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4623f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4623f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4623f-133">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="4623f-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
