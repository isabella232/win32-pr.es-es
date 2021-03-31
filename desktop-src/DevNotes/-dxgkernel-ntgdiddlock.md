---
description: Bloquea un área especificada de memoria de superficie y proporciona un puntero válido a un bloque de memoria asociado a una superficie.
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: Función NtGdiDdLock (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3ddf40ae992b6b463886396ba026ec08293bb027
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495934"
---
# <a name="ntgdiddlock-function"></a><span data-ttu-id="f1f85-103">NtGdiDdLock función)</span><span class="sxs-lookup"><span data-stu-id="f1f85-103">NtGdiDdLock function</span></span>

<span data-ttu-id="f1f85-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1f85-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f1f85-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="f1f85-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f1f85-106">Bloquea un área especificada de memoria de superficie y proporciona un puntero válido a un bloque de memoria asociado a una superficie.</span><span class="sxs-lookup"><span data-stu-id="f1f85-106">Locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f85-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1f85-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a><span data-ttu-id="f1f85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1f85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f85-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f85-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f85-110">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie asociada con la región de memoria que se va a bloquear.</span><span class="sxs-lookup"><span data-stu-id="f1f85-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="f1f85-111">*puLockData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f1f85-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f85-112">Puntero a una estructura [**DD \_ LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) que contiene la información necesaria para realizar el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f1f85-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lockdown.</span></span>

</dd> <dt>

<span data-ttu-id="f1f85-113">*hdcClip* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f85-113">*hdcClip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f85-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f1f85-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f85-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1f85-115">Return value</span></span>

<span data-ttu-id="f1f85-116">**NtGdiDdLock** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f1f85-116">**NtGdiDdLock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f1f85-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f1f85-117">Return code</span></span>                                                                                              | <span data-ttu-id="f1f85-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1f85-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1f85-119"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="f1f85-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f1f85-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="f1f85-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f1f85-121">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="f1f85-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f1f85-122">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="f1f85-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f1f85-123"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1f85-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f1f85-124">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="f1f85-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f1f85-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="f1f85-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f1f85-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f1f85-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1f85-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1f85-127">Requirements</span></span>



| <span data-ttu-id="f1f85-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1f85-128">Requirement</span></span> | <span data-ttu-id="f1f85-129">Value</span><span class="sxs-lookup"><span data-stu-id="f1f85-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f85-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f85-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f85-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f1f85-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f1f85-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1f85-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f85-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1f85-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f1f85-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1f85-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f85-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f85-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1f85-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1f85-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f85-137">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="f1f85-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
