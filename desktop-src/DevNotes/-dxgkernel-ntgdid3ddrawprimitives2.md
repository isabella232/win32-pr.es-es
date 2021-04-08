---
description: Representa primitivas y devuelve el estado de representación actualizado.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Función NtGdiD3DDrawPrimitives2 (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080135"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="25b27-103">NtGdiD3DDrawPrimitives2 función)</span><span class="sxs-lookup"><span data-stu-id="25b27-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="25b27-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="25b27-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="25b27-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="25b27-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="25b27-106">Representa primitivas y devuelve el estado de representación actualizado.</span><span class="sxs-lookup"><span data-stu-id="25b27-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="25b27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25b27-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="25b27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25b27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b27-109">*hCmdBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25b27-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-110">Identificador de la [**estructura \_ \_ local del área DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica la superficie de DirectDraw que contiene los datos del comando.</span><span class="sxs-lookup"><span data-stu-id="25b27-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-111">*hVBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25b27-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-112">Identificador de la [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que identifica la superficie de DirectDraw que contiene los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="25b27-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-113">*pded* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25b27-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-114">Puntero a una estructura de [**\_ DRAWPRIMITIVES2DATA de D3DNTHAL**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador represente una o más primitivas.</span><span class="sxs-lookup"><span data-stu-id="25b27-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-115">*pfpVidMemCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25b27-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-116">Nuevo puntero a la memoria de vídeo si el controlador intercambió el búfer de comandos.</span><span class="sxs-lookup"><span data-stu-id="25b27-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-117">*pdwSizeCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25b27-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-118">Especifica el número mínimo de bytes que el controlador debe aumentar el búfer del comando swap.</span><span class="sxs-lookup"><span data-stu-id="25b27-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-119">*pfpVidMemVtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25b27-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-120">Nuevo puntero a la memoria de vídeo si el controlador cambió el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="25b27-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="25b27-121">*pdwSizeVtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25b27-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25b27-122">Especifica el número mínimo de bytes que debe asignar el controlador para el búfer de vértices de intercambio.</span><span class="sxs-lookup"><span data-stu-id="25b27-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b27-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25b27-123">Return value</span></span>

<span data-ttu-id="25b27-124">**NtGdiD3DDrawPrimitives2** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="25b27-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="25b27-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25b27-125">Return code</span></span>                                                                                              | <span data-ttu-id="25b27-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="25b27-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25b27-127"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="25b27-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="25b27-128">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="25b27-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="25b27-129">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="25b27-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="25b27-130">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="25b27-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="25b27-131"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25b27-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="25b27-132">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="25b27-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="25b27-133">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="25b27-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="25b27-134">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25b27-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25b27-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25b27-135">Requirements</span></span>



| <span data-ttu-id="25b27-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b27-136">Requirement</span></span> | <span data-ttu-id="25b27-137">Value</span><span class="sxs-lookup"><span data-stu-id="25b27-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25b27-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25b27-138">Minimum supported client</span></span><br/> | <span data-ttu-id="25b27-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25b27-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="25b27-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25b27-140">Minimum supported server</span></span><br/> | <span data-ttu-id="25b27-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25b27-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25b27-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25b27-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b27-143"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b27-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b27-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="25b27-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b27-145">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="25b27-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
