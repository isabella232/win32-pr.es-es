---
description: Realiza una transferencia de bloque de bits.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Función NtGdiDdBlt (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 86249a8ff1069bc0875aad3fcca576ef78b9db68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153083"
---
# <a name="ntgdiddblt-function"></a><span data-ttu-id="aed6f-103">NtGdiDdBlt función)</span><span class="sxs-lookup"><span data-stu-id="aed6f-103">NtGdiDdBlt function</span></span>

<span data-ttu-id="aed6f-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aed6f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="aed6f-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="aed6f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="aed6f-106">Realiza una transferencia de bloque de bits.</span><span class="sxs-lookup"><span data-stu-id="aed6f-106">Performs a bit-block transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed6f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aed6f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a><span data-ttu-id="aed6f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aed6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed6f-109">*hSurfaceDest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aed6f-109">*hSurfaceDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed6f-110">Identificador de una [**estructura \_ \_ local de superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describe la superficie en la que se va a fundir.</span><span class="sxs-lookup"><span data-stu-id="aed6f-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface on which to blit.</span></span>

</dd> <dt>

<span data-ttu-id="aed6f-111">*hSurfaceSrc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aed6f-111">*hSurfaceSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed6f-112">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie de origen.</span><span class="sxs-lookup"><span data-stu-id="aed6f-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="aed6f-113">*puBltData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aed6f-113">*puBltData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aed6f-114">Puntero a una estructura [**DD \_ BLTDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) que contiene la información necesaria para que el controlador realice el blit.</span><span class="sxs-lookup"><span data-stu-id="aed6f-114">Pointer to a [**DD\_BLTDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) structure that contains the information required for the driver to perform the blit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed6f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aed6f-115">Return value</span></span>

<span data-ttu-id="aed6f-116">**NtGdiDdBlt** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="aed6f-116">**NtGdiDdBlt** returns one of the following callback codes.</span></span>



| <span data-ttu-id="aed6f-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aed6f-117">Return code</span></span>                                                                                              | <span data-ttu-id="aed6f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="aed6f-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aed6f-119"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="aed6f-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="aed6f-120">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="aed6f-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="aed6f-121">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="aed6f-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="aed6f-122">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="aed6f-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="aed6f-123"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aed6f-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="aed6f-124">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="aed6f-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="aed6f-125">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="aed6f-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="aed6f-126">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aed6f-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aed6f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aed6f-127">Requirements</span></span>



| <span data-ttu-id="aed6f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aed6f-128">Requirement</span></span> | <span data-ttu-id="aed6f-129">Value</span><span class="sxs-lookup"><span data-stu-id="aed6f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aed6f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aed6f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aed6f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aed6f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="aed6f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aed6f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aed6f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aed6f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aed6f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aed6f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed6f-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed6f-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed6f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="aed6f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed6f-137">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="aed6f-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
