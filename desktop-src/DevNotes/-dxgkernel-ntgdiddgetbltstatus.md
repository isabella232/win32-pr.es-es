---
description: Consulta el estado de blit de la superficie especificada.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Función NtGdiDdGetBltStatus (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 381de7f8c360f222a004786834fa36e92f1220d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659538"
---
# <a name="ntgdiddgetbltstatus-function"></a><span data-ttu-id="86f96-103">NtGdiDdGetBltStatus función)</span><span class="sxs-lookup"><span data-stu-id="86f96-103">NtGdiDdGetBltStatus function</span></span>

<span data-ttu-id="86f96-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86f96-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="86f96-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="86f96-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="86f96-106">Consulta el estado de blit de la superficie especificada.</span><span class="sxs-lookup"><span data-stu-id="86f96-106">Queries the blit status of the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f96-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86f96-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="86f96-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86f96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f96-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86f96-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f96-110">Identificador de una [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de tipo dd que representa la superficie cuyo estado de blit se está consultando.</span><span class="sxs-lookup"><span data-stu-id="86f96-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure representing the surface whose blit status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="86f96-111">*puGetBltStatusData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="86f96-111">*puGetBltStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86f96-112">Puntero a una estructura [DD \_ GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) que contiene la información necesaria para realizar la consulta de estado de blit.</span><span class="sxs-lookup"><span data-stu-id="86f96-112">Pointer to a [DD\_GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) structure that contains the information required to perform the blit status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f96-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86f96-113">Return value</span></span>

<span data-ttu-id="86f96-114">**NtGdiDdGetBltStatus** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="86f96-114">**NtGdiDdGetBltStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="86f96-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86f96-115">Return code</span></span>                                                                                              | <span data-ttu-id="86f96-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="86f96-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86f96-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="86f96-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="86f96-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="86f96-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="86f96-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="86f96-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="86f96-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="86f96-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="86f96-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="86f96-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="86f96-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="86f96-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="86f96-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="86f96-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="86f96-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="86f96-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86f96-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86f96-125">Requirements</span></span>



| <span data-ttu-id="86f96-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="86f96-126">Requirement</span></span> | <span data-ttu-id="86f96-127">Value</span><span class="sxs-lookup"><span data-stu-id="86f96-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86f96-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86f96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="86f96-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86f96-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="86f96-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86f96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="86f96-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86f96-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86f96-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86f96-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="86f96-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86f96-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f96-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f96-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f96-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="86f96-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




