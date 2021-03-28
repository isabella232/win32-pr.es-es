---
description: Establece los Estados de ocultación y siempre visible de la barra de tareas de Windows.
title: Mensaje de ABM_SETSTATE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984382"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="db2a8-103">Mensaje de ABN \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="db2a8-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="db2a8-104">Establece los Estados de ocultación y siempre visible de la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="db2a8-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="db2a8-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db2a8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db2a8-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="db2a8-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="db2a8-107">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="db2a8-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="db2a8-108">Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="db2a8-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="db2a8-109">Los datos para el estado deseado se envían en el miembro **lParam** con uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="db2a8-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="db2a8-110"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="db2a8-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="db2a8-111">Ocultar automáticamente y siempre en la parte superior desactivado</span><span class="sxs-lookup"><span data-stu-id="db2a8-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="db2a8-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**</span><span class="sxs-lookup"><span data-stu-id="db2a8-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="db2a8-113">Siempre en la parte superior, ocultar automáticamente desactivado</span><span class="sxs-lookup"><span data-stu-id="db2a8-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="db2a8-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_Ocultar automáticamente ABS**</span><span class="sxs-lookup"><span data-stu-id="db2a8-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="db2a8-115">Ocultar automáticamente en, siempre en la parte superior</span><span class="sxs-lookup"><span data-stu-id="db2a8-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="db2a8-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ AutoHide \| ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="db2a8-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="db2a8-117">Ocultar automáticamente y siempre visible en</span><span class="sxs-lookup"><span data-stu-id="db2a8-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db2a8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db2a8-118">Return value</span></span>

<span data-ttu-id="db2a8-119">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="db2a8-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2a8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db2a8-120">Requirements</span></span>



| <span data-ttu-id="db2a8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db2a8-121">Requirement</span></span> | <span data-ttu-id="db2a8-122">Value</span><span class="sxs-lookup"><span data-stu-id="db2a8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db2a8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db2a8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db2a8-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="db2a8-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db2a8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db2a8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db2a8-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db2a8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db2a8-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db2a8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db2a8-128"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="db2a8-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




