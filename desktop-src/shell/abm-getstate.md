---
description: Recupera los Estados de ocultación y siempre visible de la barra de tareas de Windows.
title: Mensaje de ABM_GETSTATE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360173"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="3cf4e-103">ABN \_ GETSTATE</span><span class="sxs-lookup"><span data-stu-id="3cf4e-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="3cf4e-104">Recupera los Estados de ocultación y siempre visible de la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="3cf4e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cf4e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf4e-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="3cf4e-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf4e-107">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="3cf4e-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="3cf4e-108">Debe especificar el miembro **cbSize** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf4e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cf4e-109">Return value</span></span>

<span data-ttu-id="3cf4e-110">Devuelve cero si la barra de tareas no está en el estado de ocultar automáticamente ni siempre visible.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="3cf4e-111">De lo contrario, el valor devuelto es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3cf4e-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cf4e-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3cf4e-112">Return code</span></span></th>
<th><span data-ttu-id="3cf4e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cf4e-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="3cf4e-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3cf4e-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3cf4e-115">La barra de tareas está en el estado siempre visible.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3cf4e-116">A partir de Windows 7, ya no se devuelve ABS_ALWAYSONTOP porque la barra de tareas siempre está en ese estado.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="3cf4e-117">El código anterior debe actualizarse para omitir la ausencia de este valor en no suponer que el valor devuelto para significa que la barra de tareas no está en el estado siempre visible.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3cf4e-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3cf4e-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3cf4e-119">La barra de tareas se encuentra en el estado de ocultar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3cf4e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf4e-120">Requirements</span></span>



| <span data-ttu-id="3cf4e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf4e-121">Requirement</span></span> | <span data-ttu-id="3cf4e-122">Value</span><span class="sxs-lookup"><span data-stu-id="3cf4e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf4e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf4e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf4e-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3cf4e-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3cf4e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf4e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf4e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3cf4e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cf4e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cf4e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf4e-128"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf4e-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




