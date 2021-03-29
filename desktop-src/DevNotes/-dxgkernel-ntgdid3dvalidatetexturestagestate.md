---
description: Devuelve el número de pasos en los que el hardware puede realizar las operaciones de combinación especificadas en el estado actual.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: Función NtGdiD3DValidateTextureStageState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907073"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="e4dad-103">NtGdiD3DValidateTextureStageState función)</span><span class="sxs-lookup"><span data-stu-id="e4dad-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="e4dad-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4dad-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e4dad-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="e4dad-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e4dad-106">Devuelve el número de pasos en los que el hardware puede realizar las operaciones de combinación especificadas en el estado actual.</span><span class="sxs-lookup"><span data-stu-id="e4dad-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4dad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4dad-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="e4dad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4dad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4dad-109">*pdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4dad-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dad-110">Puntero a una estructura de [**\_ VALIDATETEXTURESTAGESTATEDATA de D3DNTHAL**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador determine y devuelva el número de pasos necesarios para realizar las operaciones de combinación.</span><span class="sxs-lookup"><span data-stu-id="e4dad-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4dad-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4dad-111">Return value</span></span>

<span data-ttu-id="e4dad-112">**NtGdiD3DValidateTextureStageState** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e4dad-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e4dad-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e4dad-113">Return code</span></span>                                                                                              | <span data-ttu-id="e4dad-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4dad-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4dad-115"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="e4dad-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e4dad-116">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="e4dad-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e4dad-117">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="e4dad-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e4dad-118">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="e4dad-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e4dad-119"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4dad-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e4dad-120">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="e4dad-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e4dad-121">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="e4dad-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e4dad-122">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e4dad-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4dad-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4dad-123">Requirements</span></span>



| <span data-ttu-id="e4dad-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4dad-124">Requirement</span></span> | <span data-ttu-id="e4dad-125">Value</span><span class="sxs-lookup"><span data-stu-id="e4dad-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4dad-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4dad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4dad-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4dad-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e4dad-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4dad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4dad-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4dad-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e4dad-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4dad-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4dad-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4dad-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4dad-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4dad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4dad-133">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="e4dad-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
