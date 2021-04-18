---
description: Libera el bloqueo mantenido en la superficie especificada.
ms.assetid: d9d3178b-aadd-4c33-8044-8e6362f9fefe
title: Función NtGdiDdUnlock (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3472dc32cc503b83c12bcc17cdbd0d14b89b0de4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495905"
---
# <a name="ntgdiddunlock-function"></a><span data-ttu-id="854e3-103">NtGdiDdUnlock función)</span><span class="sxs-lookup"><span data-stu-id="854e3-103">NtGdiDdUnlock function</span></span>

<span data-ttu-id="854e3-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="854e3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="854e3-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="854e3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="854e3-106">Libera el bloqueo mantenido en la superficie especificada.</span><span class="sxs-lookup"><span data-stu-id="854e3-106">Releases the lock held on the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="854e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="854e3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlock(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="854e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="854e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="854e3-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="854e3-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="854e3-110">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie que se va a desbloquear.</span><span class="sxs-lookup"><span data-stu-id="854e3-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="854e3-111">*puUnlockData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="854e3-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="854e3-112">Puntero a una estructura [**DD \_ UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) que contiene la información necesaria para realizar la liberación del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="854e3-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="854e3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="854e3-113">Return value</span></span>

<span data-ttu-id="854e3-114">**NtGdiDdUnlock** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="854e3-114">**NtGdiDdUnlock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="854e3-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="854e3-115">Return code</span></span>                                                                                              | <span data-ttu-id="854e3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="854e3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="854e3-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="854e3-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="854e3-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="854e3-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="854e3-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="854e3-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="854e3-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="854e3-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="854e3-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="854e3-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="854e3-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="854e3-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="854e3-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="854e3-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="854e3-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="854e3-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="854e3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="854e3-125">Requirements</span></span>



| <span data-ttu-id="854e3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="854e3-126">Requirement</span></span> | <span data-ttu-id="854e3-127">Value</span><span class="sxs-lookup"><span data-stu-id="854e3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="854e3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="854e3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="854e3-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="854e3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="854e3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="854e3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="854e3-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="854e3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="854e3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="854e3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="854e3-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="854e3-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="854e3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="854e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854e3-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="854e3-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
