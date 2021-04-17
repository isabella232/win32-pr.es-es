---
description: Se utiliza para bloquear un área especificada de memoria de búfer y proporcionar un puntero válido a un bloque de memoria asociado al búfer.
ms.assetid: 6f2ecefa-376c-4f6c-a031-666dd992f96a
title: Función NtGdiDdLockD3D (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c049d37e3507f5bf4429b6ffd5d8ec03327640e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659663"
---
# <a name="ntgdiddlockd3d-function"></a><span data-ttu-id="dceda-103">NtGdiDdLockD3D función)</span><span class="sxs-lookup"><span data-stu-id="dceda-103">NtGdiDdLockD3D function</span></span>

<span data-ttu-id="dceda-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dceda-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dceda-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="dceda-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dceda-106">Se utiliza para bloquear un área especificada de memoria de búfer y proporcionar un puntero válido a un bloque de memoria asociado al búfer.</span><span class="sxs-lookup"><span data-stu-id="dceda-106">Used to lock a specified area of buffer memory and to provide a valid pointer to a block of memory associated with the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dceda-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dceda-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLockD3D(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData
);
```



## <a name="parameters"></a><span data-ttu-id="dceda-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dceda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dceda-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dceda-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dceda-110">Puntero a una [**estructura \_ \_ local de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describe la superficie asociada con la región de memoria que se va a bloquear.</span><span class="sxs-lookup"><span data-stu-id="dceda-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="dceda-111">*puLockData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dceda-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dceda-112">Puntero a una estructura [**DD \_ LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) que contiene la información necesaria para realizar el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="dceda-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lock down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dceda-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dceda-113">Return value</span></span>

<span data-ttu-id="dceda-114">**NtGdiDdLockD3D** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="dceda-114">**NtGdiDdLockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="dceda-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dceda-115">Return code</span></span>                                                                                              | <span data-ttu-id="dceda-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dceda-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dceda-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="dceda-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="dceda-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="dceda-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="dceda-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="dceda-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="dceda-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="dceda-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="dceda-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dceda-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="dceda-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="dceda-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="dceda-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="dceda-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="dceda-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dceda-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dceda-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dceda-125">Requirements</span></span>



| <span data-ttu-id="dceda-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dceda-126">Requirement</span></span> | <span data-ttu-id="dceda-127">Value</span><span class="sxs-lookup"><span data-stu-id="dceda-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dceda-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dceda-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dceda-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dceda-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dceda-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dceda-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dceda-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dceda-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dceda-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dceda-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dceda-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dceda-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dceda-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="dceda-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dceda-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="dceda-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
