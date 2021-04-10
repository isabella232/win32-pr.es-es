---
description: Crea una superficie de Microsoft Direct3D a partir de una superficie de Microsoft DirectDraw y le asocia un valor de identificador solicitado.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Función NtGdiDdCreateSurfaceEx (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152809"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="95888-103">NtGdiDdCreateSurfaceEx función)</span><span class="sxs-lookup"><span data-stu-id="95888-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="95888-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="95888-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="95888-105">En su lugar, use DirectDraw y Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="95888-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="95888-106">Crea una superficie de Microsoft Direct3D a partir de una superficie de Microsoft DirectDraw y le asocia un valor de identificador solicitado.</span><span class="sxs-lookup"><span data-stu-id="95888-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="95888-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95888-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="95888-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95888-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95888-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95888-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95888-110">Identificador del objeto DirectDraw creado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95888-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="95888-111">*hSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95888-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95888-112">Identificador de la superficie de DirectDraw que se va a crear para Direct3D.</span><span class="sxs-lookup"><span data-stu-id="95888-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="95888-113">Estos identificadores son únicos dentro de cada una de las distintas estructuras [**\_ \_ locales de DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) .</span><span class="sxs-lookup"><span data-stu-id="95888-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="95888-114">*dwSurfaceHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95888-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95888-115">Identificador de una estructura [**DD \_ CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) que contiene la información necesaria para que el controlador cree la superficie.</span><span class="sxs-lookup"><span data-stu-id="95888-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95888-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95888-116">Return value</span></span>

<span data-ttu-id="95888-117">**NtGdiDdCreateSurfaceEx** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="95888-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="95888-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="95888-118">Return code</span></span>                                                                                              | <span data-ttu-id="95888-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="95888-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95888-120"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="95888-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="95888-121">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="95888-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="95888-122">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="95888-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="95888-123">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="95888-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="95888-124"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95888-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="95888-125">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="95888-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="95888-126">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="95888-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="95888-127">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="95888-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="95888-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95888-128">Requirements</span></span>



| <span data-ttu-id="95888-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="95888-129">Requirement</span></span> | <span data-ttu-id="95888-130">Value</span><span class="sxs-lookup"><span data-stu-id="95888-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95888-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95888-131">Minimum supported client</span></span><br/> | <span data-ttu-id="95888-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95888-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="95888-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95888-133">Minimum supported server</span></span><br/> | <span data-ttu-id="95888-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95888-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95888-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95888-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="95888-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="95888-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95888-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="95888-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95888-138">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="95888-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
