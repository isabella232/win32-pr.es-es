---
description: Consulta la cantidad de memoria libre en el montón de memoria administrada por controlador.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: Función NtGdiD3DContextDestroyAll (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907124"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="a55a3-103">NtGdiD3DContextDestroyAll función)</span><span class="sxs-lookup"><span data-stu-id="a55a3-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="a55a3-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a55a3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a55a3-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="a55a3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a55a3-106">Consulta la cantidad de memoria libre en el montón de memoria administrada por controlador.</span><span class="sxs-lookup"><span data-stu-id="a55a3-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="a55a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a55a3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="a55a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a55a3-108">Parameters</span></span>

<span data-ttu-id="a55a3-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a55a3-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a55a3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a55a3-110">Return value</span></span>

<span data-ttu-id="a55a3-111">**NtGdiD3DContextDestroyAll** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a55a3-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a55a3-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a55a3-112">Return code</span></span>                                                                                              | <span data-ttu-id="a55a3-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a55a3-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a55a3-114"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="a55a3-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a55a3-115">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="a55a3-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a55a3-116">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="a55a3-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a55a3-117">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="a55a3-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a55a3-118"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a55a3-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a55a3-119">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a55a3-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a55a3-120">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="a55a3-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a55a3-121">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a55a3-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a55a3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a55a3-122">Requirements</span></span>



| <span data-ttu-id="a55a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a55a3-123">Requirement</span></span> | <span data-ttu-id="a55a3-124">Value</span><span class="sxs-lookup"><span data-stu-id="a55a3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a55a3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a55a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a55a3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a55a3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a55a3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a55a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a55a3-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a55a3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a55a3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a55a3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a55a3-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a55a3-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a55a3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a55a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a55a3-132">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="a55a3-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




