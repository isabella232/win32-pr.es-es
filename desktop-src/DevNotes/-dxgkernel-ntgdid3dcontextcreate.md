---
description: Crea un contexto.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Función NtGdiD3DContextCreate (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152817"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="01baa-103">NtGdiD3DContextCreate función)</span><span class="sxs-lookup"><span data-stu-id="01baa-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="01baa-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01baa-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="01baa-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="01baa-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="01baa-106">Crea un contexto.</span><span class="sxs-lookup"><span data-stu-id="01baa-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="01baa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01baa-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="01baa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01baa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01baa-109">*hDirectDrawLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01baa-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01baa-110">Identificador de un objeto de DirectDraw en modo kernel, creado anteriormente con [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), que representa el dispositivo en el que se va a crear el contexto de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01baa-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="01baa-111">*hSurfColor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01baa-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01baa-112">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie de DirectDraw que se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="01baa-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="01baa-113">*hSurfZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01baa-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01baa-114">Identificador de una [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que describe la superficie de DirectDraw que se va a usar como búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="01baa-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="01baa-115">Si este miembro es **null**, no se realizará ningún almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="01baa-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="01baa-116">*pdcci* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01baa-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01baa-117">Puntero a una estructura de [**\_ CONTEXTCREATEDATA de D3DNTHAL**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para crear un contexto y los datos que el controlador debe almacenar en el nuevo contexto.</span><span class="sxs-lookup"><span data-stu-id="01baa-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01baa-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01baa-118">Return value</span></span>

<span data-ttu-id="01baa-119">**NtGdiD3DContextCreate** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="01baa-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="01baa-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="01baa-120">Return code</span></span>                                                                                              | <span data-ttu-id="01baa-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="01baa-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01baa-122"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="01baa-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="01baa-123">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="01baa-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="01baa-124">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="01baa-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="01baa-125">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="01baa-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="01baa-126"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="01baa-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="01baa-127">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="01baa-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="01baa-128">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="01baa-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="01baa-129">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01baa-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01baa-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01baa-130">Requirements</span></span>



| <span data-ttu-id="01baa-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="01baa-131">Requirement</span></span> | <span data-ttu-id="01baa-132">Value</span><span class="sxs-lookup"><span data-stu-id="01baa-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01baa-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01baa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="01baa-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="01baa-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="01baa-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01baa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="01baa-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01baa-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01baa-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01baa-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="01baa-138"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01baa-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01baa-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="01baa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01baa-140">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="01baa-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
