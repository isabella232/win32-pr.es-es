---
description: Hace que se intercambie la memoria de la superficie asociada a las superficies de destino y actuales.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Función NtGdiDdFlip (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907214"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="14250-103">NtGdiDdFlip función)</span><span class="sxs-lookup"><span data-stu-id="14250-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="14250-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="14250-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="14250-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="14250-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="14250-106">Hace que se intercambie la memoria de la superficie asociada a las superficies de destino y actuales.</span><span class="sxs-lookup"><span data-stu-id="14250-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="14250-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14250-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="14250-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14250-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14250-109">*hSurfaceCurrent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14250-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14250-110">Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie actual.</span><span class="sxs-lookup"><span data-stu-id="14250-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="14250-111">*hSurfaceTarget* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14250-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14250-112">Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie de destino; es decir, la superficie en la que se debe voltear el controlador.</span><span class="sxs-lookup"><span data-stu-id="14250-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="14250-113">*hSurfaceCurrentLeft* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14250-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14250-114">Identificador de la [estructura \_ \_ local del área DD](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie izquierda actual.</span><span class="sxs-lookup"><span data-stu-id="14250-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="14250-115">*hSurfaceTargetLeft* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14250-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14250-116">Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie de destino de la izquierda a la que se va a voltear.</span><span class="sxs-lookup"><span data-stu-id="14250-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="14250-117">*puFlipData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14250-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14250-118">Puntero a una estructura [DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) que contiene la información necesaria para realizar el volteo.</span><span class="sxs-lookup"><span data-stu-id="14250-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14250-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14250-119">Return value</span></span>

<span data-ttu-id="14250-120">**NtGdiDdFlip** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="14250-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="14250-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="14250-121">Return code</span></span>                                                                                              | <span data-ttu-id="14250-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="14250-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14250-123"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="14250-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="14250-124">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="14250-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="14250-125">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="14250-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="14250-126">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="14250-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="14250-127"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14250-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="14250-128">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="14250-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="14250-129">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="14250-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="14250-130">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="14250-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14250-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14250-131">Requirements</span></span>



| <span data-ttu-id="14250-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="14250-132">Requirement</span></span> | <span data-ttu-id="14250-133">Value</span><span class="sxs-lookup"><span data-stu-id="14250-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14250-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14250-134">Minimum supported client</span></span><br/> | <span data-ttu-id="14250-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14250-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="14250-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14250-136">Minimum supported server</span></span><br/> | <span data-ttu-id="14250-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14250-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14250-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14250-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="14250-139"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="14250-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14250-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="14250-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14250-141">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="14250-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




