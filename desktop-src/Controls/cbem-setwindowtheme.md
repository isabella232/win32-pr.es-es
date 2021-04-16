---
title: Mensaje de CBEM_SETWINDOWTHEME (commctrl. h)
description: Establece el estilo visual de un control ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- CBEM_SETWINDOWTHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658221"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="fe221-104">CBEM \_ SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="fe221-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="fe221-105">Establece el estilo visual de un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="fe221-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe221-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe221-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe221-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe221-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe221-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fe221-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe221-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe221-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe221-110">Puntero a una cadena Unicode que contiene el estilo visual de control que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="fe221-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe221-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe221-111">Return value</span></span>

<span data-ttu-id="fe221-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="fe221-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe221-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe221-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe221-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique la versión 6,0 de Comclt32.</span><span class="sxs-lookup"><span data-stu-id="fe221-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="fe221-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fe221-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe221-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe221-116">Requirements</span></span>



| <span data-ttu-id="fe221-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe221-117">Requirement</span></span> | <span data-ttu-id="fe221-118">Value</span><span class="sxs-lookup"><span data-stu-id="fe221-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe221-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe221-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe221-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe221-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe221-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe221-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe221-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe221-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe221-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe221-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe221-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe221-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





