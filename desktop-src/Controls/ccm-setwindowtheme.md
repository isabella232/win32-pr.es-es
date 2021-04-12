---
title: Mensaje de CCM_SETWINDOWTHEME (commctrl. h)
description: Establece el estilo visual de un control.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491524"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="729b3-104">\_Mensaje SETWINDOWTHEME de CCM</span><span class="sxs-lookup"><span data-stu-id="729b3-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="729b3-105">Establece el estilo visual de un control.</span><span class="sxs-lookup"><span data-stu-id="729b3-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="729b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="729b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="729b3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="729b3-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="729b3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="729b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="729b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="729b3-110">Puntero a una cadena Unicode que contiene el estilo visual de control que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="729b3-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729b3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="729b3-111">Return value</span></span>

<span data-ttu-id="729b3-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="729b3-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="729b3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="729b3-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="729b3-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="729b3-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="729b3-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="729b3-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="729b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="729b3-116">Requirements</span></span>



| <span data-ttu-id="729b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="729b3-117">Requirement</span></span> | <span data-ttu-id="729b3-118">Value</span><span class="sxs-lookup"><span data-stu-id="729b3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="729b3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="729b3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="729b3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="729b3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="729b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="729b3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="729b3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="729b3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="729b3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="729b3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="729b3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





