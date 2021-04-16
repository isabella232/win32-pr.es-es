---
description: Determina si el controlador puede crear un comando de nivel de controlador o un búfer de vértice de la descripción especificada.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: Función NtGdiDdCanCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648163"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="257cb-103">NtGdiDdCanCreateD3DBuffer función)</span><span class="sxs-lookup"><span data-stu-id="257cb-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="257cb-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="257cb-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="257cb-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="257cb-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="257cb-106">Determina si el controlador puede crear un comando de nivel de controlador o un búfer de vértice de la descripción especificada.</span><span class="sxs-lookup"><span data-stu-id="257cb-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="257cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="257cb-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="257cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="257cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="257cb-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="257cb-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="257cb-110">Identificador de la [**estructura \_ \_ global DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el objeto DIRECTDRAW.</span><span class="sxs-lookup"><span data-stu-id="257cb-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="257cb-111">*puCanCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="257cb-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="257cb-112">Puntero a una estructura [**DD \_ CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) .</span><span class="sxs-lookup"><span data-stu-id="257cb-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="257cb-113">Esta estructura contiene la información necesaria para que el controlador determine si se puede crear un búfer de comandos o de vértices.</span><span class="sxs-lookup"><span data-stu-id="257cb-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="257cb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="257cb-114">Return value</span></span>

<span data-ttu-id="257cb-115">**NtGdiDdCanCreateD3DBuffer** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="257cb-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="257cb-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="257cb-116">Return code</span></span>                                                                                              | <span data-ttu-id="257cb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="257cb-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="257cb-118"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="257cb-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="257cb-119">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="257cb-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="257cb-120">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="257cb-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="257cb-121">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="257cb-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="257cb-122"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="257cb-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="257cb-123">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="257cb-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="257cb-124">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="257cb-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="257cb-125">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="257cb-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="257cb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="257cb-126">Requirements</span></span>



| <span data-ttu-id="257cb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="257cb-127">Requirement</span></span> | <span data-ttu-id="257cb-128">Value</span><span class="sxs-lookup"><span data-stu-id="257cb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="257cb-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="257cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="257cb-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="257cb-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="257cb-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="257cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="257cb-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="257cb-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="257cb-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="257cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="257cb-134"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="257cb-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257cb-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="257cb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257cb-136">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="257cb-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
