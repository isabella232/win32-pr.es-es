---
description: Destruye un objeto Surface de Microsoft DirectDraw de modo kernel previamente asignado.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Función NtGdiDdDestroySurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080191"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="bd218-103">NtGdiDdDestroySurface función)</span><span class="sxs-lookup"><span data-stu-id="bd218-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="bd218-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bd218-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bd218-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="bd218-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bd218-106">Destruye un objeto Surface de Microsoft DirectDraw de modo kernel previamente asignado.</span><span class="sxs-lookup"><span data-stu-id="bd218-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd218-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd218-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="bd218-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd218-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd218-109">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd218-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd218-110">Identificador del objeto de superficie en modo kernel previamente asignado.</span><span class="sxs-lookup"><span data-stu-id="bd218-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="bd218-111">*bRealDestroy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd218-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd218-112">Especifica cómo destruir la superficie.</span><span class="sxs-lookup"><span data-stu-id="bd218-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="bd218-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bd218-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="bd218-114">REALES</span><span class="sxs-lookup"><span data-stu-id="bd218-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="bd218-115">Destruya la superficie y la memoria de vídeo libre.</span><span class="sxs-lookup"><span data-stu-id="bd218-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="bd218-116">ES</span><span class="sxs-lookup"><span data-stu-id="bd218-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="bd218-117">Libere la memoria de vídeo pero deje la superficie en un estado no inicializado.</span><span class="sxs-lookup"><span data-stu-id="bd218-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd218-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd218-118">Return value</span></span>

<span data-ttu-id="bd218-119">**NtGdiDdDestroySurface** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bd218-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="bd218-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd218-120">Return code</span></span>                                                                                              | <span data-ttu-id="bd218-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd218-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd218-122"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd218-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="bd218-123">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="bd218-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="bd218-124">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="bd218-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="bd218-125">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="bd218-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="bd218-126"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bd218-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="bd218-127">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bd218-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="bd218-128">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="bd218-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="bd218-129">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bd218-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd218-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd218-130">Remarks</span></span>

<span data-ttu-id="bd218-131">Se recomienda que las aplicaciones usen las API de DirectDraw y Direct3D para crear y destruir superficies en lugar de esta función.</span><span class="sxs-lookup"><span data-stu-id="bd218-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd218-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd218-132">Requirements</span></span>



| <span data-ttu-id="bd218-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd218-133">Requirement</span></span> | <span data-ttu-id="bd218-134">Value</span><span class="sxs-lookup"><span data-stu-id="bd218-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd218-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd218-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bd218-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bd218-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bd218-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd218-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bd218-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd218-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd218-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd218-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd218-140"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd218-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd218-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd218-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd218-142">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="bd218-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




