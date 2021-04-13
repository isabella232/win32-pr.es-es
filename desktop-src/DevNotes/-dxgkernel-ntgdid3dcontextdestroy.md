---
description: Elimina el contexto especificado.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: Función NtGdiD3DContextDestroy (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 19799c3895072011dd104deec18664d1ffc52b9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538878"
---
# <a name="ntgdid3dcontextdestroy-function"></a><span data-ttu-id="e36a1-103">NtGdiD3DContextDestroy función)</span><span class="sxs-lookup"><span data-stu-id="e36a1-103">NtGdiD3DContextDestroy function</span></span>

<span data-ttu-id="e36a1-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e36a1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e36a1-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="e36a1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e36a1-106">Elimina el contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="e36a1-106">Deletes the specified context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e36a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e36a1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a><span data-ttu-id="e36a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e36a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e36a1-109">*pContextDestroyData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e36a1-109">*pContextDestroyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e36a1-110">Puntero a una estructura de [**\_ CONTEXTDESTROYDATA de D3DNTHAL**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador destruya el contexto.</span><span class="sxs-lookup"><span data-stu-id="e36a1-110">Pointer to a [**D3DNTHAL\_CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to destroy the context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e36a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e36a1-111">Return value</span></span>

<span data-ttu-id="e36a1-112">**NtGdiD3DContextDestroy** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e36a1-112">**NtGdiD3DContextDestroy** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e36a1-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e36a1-113">Return code</span></span>                                                                                              | <span data-ttu-id="e36a1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e36a1-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e36a1-115"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a1-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e36a1-116">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="e36a1-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e36a1-117">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="e36a1-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e36a1-118">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="e36a1-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e36a1-119"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a1-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e36a1-120">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="e36a1-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e36a1-121">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="e36a1-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e36a1-122">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e36a1-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e36a1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e36a1-123">Requirements</span></span>



| <span data-ttu-id="e36a1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e36a1-124">Requirement</span></span> | <span data-ttu-id="e36a1-125">Value</span><span class="sxs-lookup"><span data-stu-id="e36a1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e36a1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e36a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e36a1-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e36a1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e36a1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e36a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e36a1-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e36a1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e36a1-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e36a1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e36a1-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e36a1-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e36a1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e36a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e36a1-133">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="e36a1-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
