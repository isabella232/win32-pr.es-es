---
description: Adjunta dos representaciones de superficie en modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Función NtGdiDdAttachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659427"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="e15a6-103">NtGdiDdAttachSurface función)</span><span class="sxs-lookup"><span data-stu-id="e15a6-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="e15a6-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e15a6-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e15a6-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="e15a6-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e15a6-106">Adjunta dos representaciones de superficie en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="e15a6-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e15a6-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="e15a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e15a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e15a6-109">*hSurfaceFrom* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e15a6-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e15a6-110">Identificador del objeto de superficie de modo kernel que será el punto de inicio de los nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e15a6-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="e15a6-111">*hSurfaceTo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e15a6-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e15a6-112">Identificador del objeto de superficie de modo kernel que será el punto final de los nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e15a6-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e15a6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e15a6-113">Return value</span></span>

<span data-ttu-id="e15a6-114">**NtGdiDdAttachSurface** devuelve uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e15a6-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="e15a6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e15a6-115">Return code</span></span>                                                                          | <span data-ttu-id="e15a6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e15a6-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e15a6-117"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="e15a6-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="e15a6-118">La llamada de función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e15a6-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="e15a6-119"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="e15a6-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e15a6-120">Error en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="e15a6-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e15a6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e15a6-121">Remarks</span></span>

<span data-ttu-id="e15a6-122">Vea el kit de desarrollo de software (SDK) de DirectDraw y el kit de desarrollo de controladores (DDK) para obtener una descripción completa de los datos adjuntos de la superficie.</span><span class="sxs-lookup"><span data-stu-id="e15a6-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="e15a6-123">Como con otros datos adjuntos de la superficie, los datos adjuntos resultantes son unidireccionales.</span><span class="sxs-lookup"><span data-stu-id="e15a6-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="e15a6-124">Después de llamar a esta función, *hSurfaceTo* no se adjuntará a *hSurfaceFrom*.</span><span class="sxs-lookup"><span data-stu-id="e15a6-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e15a6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e15a6-125">Requirements</span></span>



| <span data-ttu-id="e15a6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e15a6-126">Requirement</span></span> | <span data-ttu-id="e15a6-127">Value</span><span class="sxs-lookup"><span data-stu-id="e15a6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e15a6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e15a6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e15a6-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e15a6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e15a6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e15a6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e15a6-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e15a6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e15a6-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e15a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e15a6-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e15a6-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e15a6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e15a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15a6-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="e15a6-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




