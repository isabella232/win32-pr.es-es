---
description: Notifica al controlador que este objeto de compensación de movimiento ya no se usará. Ahora, el controlador debe realizar cualquier limpieza necesaria.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Función NtGdiDdDestroyMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907123"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="c5221-104">NtGdiDdDestroyMoComp función)</span><span class="sxs-lookup"><span data-stu-id="c5221-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="c5221-105">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c5221-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="c5221-106">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="c5221-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="c5221-107">Notifica al controlador que este objeto de compensación de movimiento ya no se usará.</span><span class="sxs-lookup"><span data-stu-id="c5221-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="c5221-108">Ahora, el controlador debe realizar cualquier limpieza necesaria.</span><span class="sxs-lookup"><span data-stu-id="c5221-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5221-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5221-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="c5221-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5221-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5221-111">*hMoComp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5221-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5221-112">Identificador de una [**estructura \_ \_ local DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contiene una descripción del objeto de compensación de movimiento que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="c5221-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="c5221-113">*puBeginFrameData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c5221-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5221-114">Puntero a una estructura [**DD \_ DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) que contiene la información necesaria para finalizar la compensación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="c5221-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5221-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5221-115">Return value</span></span>

<span data-ttu-id="c5221-116">**NtGdiDdDestroyMoComp** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c5221-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="c5221-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c5221-117">Return code</span></span>                                                                                              | <span data-ttu-id="c5221-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5221-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5221-119"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="c5221-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="c5221-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="c5221-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="c5221-121">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="c5221-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="c5221-122">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="c5221-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c5221-123"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5221-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="c5221-124">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="c5221-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="c5221-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="c5221-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="c5221-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c5221-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5221-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5221-127">Remarks</span></span>

<span data-ttu-id="c5221-128">Para obtener más información, vea el kit de desarrollo de controladores (DDK) de Microsoft DirectX video Acceleration.</span><span class="sxs-lookup"><span data-stu-id="c5221-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5221-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5221-129">Requirements</span></span>



| <span data-ttu-id="c5221-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5221-130">Requirement</span></span> | <span data-ttu-id="c5221-131">Value</span><span class="sxs-lookup"><span data-stu-id="c5221-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5221-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5221-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c5221-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5221-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c5221-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5221-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c5221-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5221-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5221-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5221-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5221-137"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5221-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5221-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5221-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5221-139">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="c5221-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
