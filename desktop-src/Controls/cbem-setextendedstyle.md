---
title: Mensaje de CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Establece los estilos extendidos dentro de un control ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658379"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="9a645-104">CBEM \_ SETEXTENDEDSTYLE</span><span class="sxs-lookup"><span data-stu-id="9a645-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="9a645-105">Establece los estilos extendidos dentro de un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="9a645-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a645-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a645-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a645-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a645-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a645-108">Valor **DWORD** que indica qué estilos de *lParam* se van a ver afectados.</span><span class="sxs-lookup"><span data-stu-id="9a645-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="9a645-109">Solo se cambiarán los estilos extendidos de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9a645-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="9a645-110">Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9a645-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="9a645-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a645-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a645-112">Valor **DWORD** que contiene los [estilos extendidos del control ComboBoxEx](comboboxex-control-extended-styles.md) que se van a establecer para el control.</span><span class="sxs-lookup"><span data-stu-id="9a645-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a645-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a645-113">Return value</span></span>

<span data-ttu-id="9a645-114">Devuelve un valor **DWORD** que contiene los estilos extendidos utilizados previamente para el control.</span><span class="sxs-lookup"><span data-stu-id="9a645-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a645-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a645-115">Remarks</span></span>

<span data-ttu-id="9a645-116">*wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes.</span><span class="sxs-lookup"><span data-stu-id="9a645-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="9a645-117">Por ejemplo, si pasa [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **CBES \_ ex \_ NOEDITIMAGE** , pero el resto de los estilos permanecerán iguales.</span><span class="sxs-lookup"><span data-stu-id="9a645-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="9a645-118">Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo [**\_ simple CBS**](combo-box-styles.md) , es posible que no se vuelva a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a645-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a645-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a645-119">Requirements</span></span>



| <span data-ttu-id="9a645-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a645-120">Requirement</span></span> | <span data-ttu-id="9a645-121">Value</span><span class="sxs-lookup"><span data-stu-id="9a645-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a645-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a645-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a645-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a645-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a645-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a645-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a645-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a645-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a645-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a645-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a645-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a645-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





