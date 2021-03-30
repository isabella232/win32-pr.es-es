---
title: Mensaje de LVM_SETOUTLINECOLOR (commctrl. h)
description: Establece el color del borde de un control de vista de lista si \_ \_ se establece el estilo de ventana extendida LVS ex BORDERSELECT.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905003"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="4f8e8-104">\_Mensaje SETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="4f8e8-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="4f8e8-105">Establece el color del borde de un control de vista de lista si se establece el estilo de ventana extendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4f8e8-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f8e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f8e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f8e8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4f8e8-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4f8e8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4f8e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f8e8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4f8e8-110">Estructura **COLORREF** que especifica el color para establecer el borde.</span><span class="sxs-lookup"><span data-stu-id="4f8e8-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8e8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f8e8-111">Return value</span></span>

<span data-ttu-id="4f8e8-112">Devuelve la estructura **COLORREF** que contiene el color del contorno.</span><span class="sxs-lookup"><span data-stu-id="4f8e8-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8e8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f8e8-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f8e8-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="4f8e8-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4f8e8-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f8e8-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f8e8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f8e8-116">Requirements</span></span>



| <span data-ttu-id="4f8e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8e8-117">Requirement</span></span> | <span data-ttu-id="4f8e8-118">Value</span><span class="sxs-lookup"><span data-stu-id="4f8e8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8e8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f8e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8e8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4f8e8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f8e8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f8e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8e8-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f8e8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f8e8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f8e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8e8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8e8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





