---
description: Lo usan los tiempos de ejecución de Microsoft DirectDraw y Microsoft Direct3D para obtener información del controlador sobre su estado actual.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: Función NtGdiD3DGetDriverState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659351"
---
# <a name="ntgdid3dgetdriverstate-function"></a><span data-ttu-id="750ff-103">NtGdiD3DGetDriverState función)</span><span class="sxs-lookup"><span data-stu-id="750ff-103">NtGdiD3DGetDriverState function</span></span>

<span data-ttu-id="750ff-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="750ff-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="750ff-105">En su lugar, use DirectDraw y Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="750ff-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="750ff-106">Lo usan los tiempos de ejecución de Microsoft DirectDraw y Microsoft Direct3D para obtener información del controlador sobre su estado actual.</span><span class="sxs-lookup"><span data-stu-id="750ff-106">Used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="750ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="750ff-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a><span data-ttu-id="750ff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="750ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750ff-109">*pdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="750ff-109">*pdata* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="750ff-110">Puntero a una estructura [**DD \_ GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) que describe el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="750ff-110">Pointer to a [**DD\_GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) structure that describes the state of the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750ff-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="750ff-111">Return value</span></span>

<span data-ttu-id="750ff-112">**NtGdiD3DGetDriverState** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="750ff-112">**NtGdiD3DGetDriverState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="750ff-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="750ff-113">Return code</span></span>                                                                                              | <span data-ttu-id="750ff-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="750ff-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="750ff-115"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="750ff-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="750ff-116">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="750ff-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="750ff-117">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="750ff-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="750ff-118">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="750ff-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="750ff-119"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="750ff-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="750ff-120">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="750ff-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="750ff-121">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="750ff-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="750ff-122">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="750ff-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="750ff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="750ff-123">Requirements</span></span>



| <span data-ttu-id="750ff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="750ff-124">Requirement</span></span> | <span data-ttu-id="750ff-125">Value</span><span class="sxs-lookup"><span data-stu-id="750ff-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="750ff-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="750ff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="750ff-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="750ff-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="750ff-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="750ff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="750ff-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="750ff-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="750ff-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="750ff-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="750ff-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="750ff-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750ff-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="750ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750ff-133">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="750ff-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
