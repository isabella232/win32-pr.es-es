---
title: Mensaje de TB_SETWINDOWTHEME (commctrl. h)
description: Establece el estilo visual de un control de barra de herramientas.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- TB_SETWINDOWTHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151253"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="f15b1-104">\_Mensaje SETWINDOWTHEME TB</span><span class="sxs-lookup"><span data-stu-id="f15b1-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="f15b1-105">Establece el estilo visual de un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f15b1-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f15b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f15b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f15b1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f15b1-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f15b1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f15b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f15b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f15b1-110">Puntero a una cadena Unicode que contiene el estilo visual de la barra de herramientas que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f15b1-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15b1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f15b1-111">Return value</span></span>

<span data-ttu-id="f15b1-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f15b1-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15b1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f15b1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f15b1-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f15b1-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f15b1-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f15b1-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="f15b1-116">Enviar este mensaje es equivalente a llamar a [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) en la barra de herramientas y su control ToolTip, si existe.</span><span class="sxs-lookup"><span data-stu-id="f15b1-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f15b1-117">Requirements</span></span>



| <span data-ttu-id="f15b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15b1-118">Requirement</span></span> | <span data-ttu-id="f15b1-119">Value</span><span class="sxs-lookup"><span data-stu-id="f15b1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f15b1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f15b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f15b1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f15b1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f15b1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f15b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f15b1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f15b1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f15b1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f15b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f15b1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15b1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





