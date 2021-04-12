---
title: Mensaje de LVM_MAPINDEXTOID (commctrl. h)
description: Asigna el índice de un elemento a un identificador único.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489982"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="156bc-104">\_Mensaje MAPINDEXTOID LVM</span><span class="sxs-lookup"><span data-stu-id="156bc-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="156bc-105">Asigna el índice de un elemento a un identificador único.</span><span class="sxs-lookup"><span data-stu-id="156bc-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="156bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="156bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="156bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-108">Índice de un elemento.</span><span class="sxs-lookup"><span data-stu-id="156bc-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="156bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="156bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="156bc-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="156bc-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="156bc-111">Return value</span></span>

<span data-ttu-id="156bc-112">Devuelve un identificador único.</span><span class="sxs-lookup"><span data-stu-id="156bc-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="156bc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="156bc-113">Remarks</span></span>

<span data-ttu-id="156bc-114">Los controles de vista de lista controlan internamente los elementos por índice.</span><span class="sxs-lookup"><span data-stu-id="156bc-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="156bc-115">Esto puede presentar problemas porque los índices pueden cambiar durante la duración del control.</span><span class="sxs-lookup"><span data-stu-id="156bc-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="156bc-116">El control de vista de lista puede etiquetar un elemento con un identificador cuando se crea el elemento.</span><span class="sxs-lookup"><span data-stu-id="156bc-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="156bc-117">Puede usar este identificador para garantizar la exclusividad durante la duración del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="156bc-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="156bc-118">Para identificar de forma única un elemento, tome el índice devuelto por una llamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a **LVM \_ MAPINDEXTOID**.</span><span class="sxs-lookup"><span data-stu-id="156bc-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="156bc-119">El valor devuelto es un identificador único.</span><span class="sxs-lookup"><span data-stu-id="156bc-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="156bc-120">En un entorno multiproceso, el índice solo se garantiza en el subproceso que hospeda el control de vista de lista, no en los subprocesos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="156bc-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="156bc-121">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="156bc-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="156bc-122">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="156bc-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="156bc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="156bc-123">Requirements</span></span>



| <span data-ttu-id="156bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="156bc-124">Requirement</span></span> | <span data-ttu-id="156bc-125">Value</span><span class="sxs-lookup"><span data-stu-id="156bc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="156bc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="156bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="156bc-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="156bc-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="156bc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="156bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="156bc-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="156bc-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="156bc-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="156bc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="156bc-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="156bc-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

