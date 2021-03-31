---
title: Mensaje de LVM_SETICONSPACING (commctrl. h)
description: Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo de icono de LVS \_ . Puede enviar este mensaje explícitamente o mediante la \_ macro SetIconSpacing de ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905004"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="c8861-105">\_Mensaje SETICONSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="c8861-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="c8861-106">Establece el espaciado entre los iconos de los controles de vista de lista que tienen el estilo de [**\_ icono de LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c8861-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="c8861-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetIconSpacing de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .</span><span class="sxs-lookup"><span data-stu-id="c8861-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8861-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8861-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8861-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8861-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8861-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c8861-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8861-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8861-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8861-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la distancia, en píxeles, que se va a establecer entre los iconos del eje x.</span><span class="sxs-lookup"><span data-stu-id="c8861-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="c8861-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la distancia, en píxeles, que se va a establecer entre los iconos del eje y.</span><span class="sxs-lookup"><span data-stu-id="c8861-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="c8861-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c8861-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8861-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8861-115">Return value</span></span>

<span data-ttu-id="c8861-116">Devuelve un valor **DWORD** que contiene la distancia del eje x anterior en la palabra baja y la distancia del eje y anterior en la palabra alta.</span><span class="sxs-lookup"><span data-stu-id="c8861-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8861-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8861-117">Remarks</span></span>

<span data-ttu-id="c8861-118">Los valores de *lParam* son relativos a la esquina superior izquierda de un mapa de bits de icono.</span><span class="sxs-lookup"><span data-stu-id="c8861-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="c8861-119">Por lo tanto, para establecer el espaciado entre los iconos que no se superponen, los valores *lParam* deben incluir el tamaño del icono, más la cantidad de espacio vacío deseado entre los iconos.</span><span class="sxs-lookup"><span data-stu-id="c8861-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="c8861-120">Los valores que no incluyen el ancho del icono darán lugar a superposiciones.</span><span class="sxs-lookup"><span data-stu-id="c8861-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="c8861-121">Al definir el espaciado de los iconos, los valores *lParam* deben establecerse en 4 o más.</span><span class="sxs-lookup"><span data-stu-id="c8861-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="c8861-122">Los valores más pequeños no producirán el diseño deseado.</span><span class="sxs-lookup"><span data-stu-id="c8861-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="c8861-123">Para restablecer los iconos en el espaciado predeterminado, establezca los valores de *lParam* en-1.</span><span class="sxs-lookup"><span data-stu-id="c8861-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8861-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8861-124">Requirements</span></span>



| <span data-ttu-id="c8861-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8861-125">Requirement</span></span> | <span data-ttu-id="c8861-126">Value</span><span class="sxs-lookup"><span data-stu-id="c8861-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8861-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8861-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8861-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c8861-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8861-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8861-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8861-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8861-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8861-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8861-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8861-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8861-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

