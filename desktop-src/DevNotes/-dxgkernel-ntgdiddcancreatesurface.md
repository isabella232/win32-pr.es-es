---
description: Indica si el controlador puede crear una superficie de la descripción de la superficie especificada.
ms.assetid: 4626163b-3070-4246-9a04-0b3438fc7057
title: Función NtGdiDdCanCreateSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c45f3e93bff409f68e5ba7fbe441a398e80b0e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495911"
---
# <a name="ntgdiddcancreatesurface-function"></a><span data-ttu-id="81794-103">NtGdiDdCanCreateSurface función)</span><span class="sxs-lookup"><span data-stu-id="81794-103">NtGdiDdCanCreateSurface function</span></span>

<span data-ttu-id="81794-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="81794-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="81794-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="81794-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="81794-106">Indica si el controlador puede crear una superficie de la descripción de la superficie especificada.</span><span class="sxs-lookup"><span data-stu-id="81794-106">Indicates whether the driver can create a surface of the specified surface description.</span></span>

## <a name="syntax"></a><span data-ttu-id="81794-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81794-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateSurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="81794-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81794-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81794-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81794-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81794-110">Identificador de la [**estructura \_ \_ global DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el objeto DIRECTDRAW.</span><span class="sxs-lookup"><span data-stu-id="81794-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="81794-111">*puCanCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81794-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81794-112">Puntero a una estructura de [**\_ CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) de tipo dd que contiene la información necesaria para que el controlador determine si se puede crear una superficie.</span><span class="sxs-lookup"><span data-stu-id="81794-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure containing the information required for the driver to determine whether a surface can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81794-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81794-113">Return value</span></span>

<span data-ttu-id="81794-114">**NtGdiDdCanCreateSurface** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="81794-114">**NtGdiDdCanCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="81794-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="81794-115">Return code</span></span>                                                                                              | <span data-ttu-id="81794-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="81794-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81794-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="81794-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="81794-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="81794-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="81794-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="81794-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="81794-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="81794-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="81794-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81794-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="81794-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="81794-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="81794-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="81794-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="81794-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="81794-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81794-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81794-125">Requirements</span></span>



| <span data-ttu-id="81794-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="81794-126">Requirement</span></span> | <span data-ttu-id="81794-127">Value</span><span class="sxs-lookup"><span data-stu-id="81794-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81794-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81794-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81794-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81794-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="81794-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81794-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81794-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81794-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="81794-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81794-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="81794-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="81794-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81794-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81794-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81794-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="81794-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
