---
title: Mensaje de LVM_MAPIDTOINDEX (commctrl. h)
description: Asigna el identificador de un elemento a un índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658321"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="e0648-104">\_Mensaje MAPIDTOINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="e0648-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="e0648-105">Asigna el identificador de un elemento a un índice.</span><span class="sxs-lookup"><span data-stu-id="e0648-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0648-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0648-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0648-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0648-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0648-108">IDENTIFICADOR único de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e0648-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="e0648-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0648-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0648-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e0648-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0648-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0648-111">Return value</span></span>

<span data-ttu-id="e0648-112">Devuelve el índice más actual.</span><span class="sxs-lookup"><span data-stu-id="e0648-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0648-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0648-113">Remarks</span></span>

<span data-ttu-id="e0648-114">Los controles de vista de lista controlan internamente los elementos por índice.</span><span class="sxs-lookup"><span data-stu-id="e0648-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="e0648-115">Esto puede presentar problemas porque los índices pueden cambiar durante la duración del control.</span><span class="sxs-lookup"><span data-stu-id="e0648-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="e0648-116">El control de vista de lista puede etiquetar un elemento con un identificador cuando se crea el elemento.</span><span class="sxs-lookup"><span data-stu-id="e0648-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="e0648-117">Puede usar este identificador para garantizar la exclusividad durante la duración del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="e0648-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="e0648-118">Para identificar de forma única un elemento, tome el índice devuelto por una llamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) y llame a [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="e0648-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="e0648-119">El valor devuelto es un identificador único.</span><span class="sxs-lookup"><span data-stu-id="e0648-119">The return value is a unique ID.</span></span>

<span data-ttu-id="e0648-120">Si necesita el índice de un elemento una vez creado un identificador, puede llamar a **LVM \_ MAPIDTOINDEX** con el identificador único y devuelve el índice más actual.</span><span class="sxs-lookup"><span data-stu-id="e0648-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="e0648-121">**LVM \_ MAPIDTOINDEX** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e0648-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="e0648-122">En un entorno multiproceso, el índice solo se garantiza en el subproceso que hospeda el control de vista de lista, no en los subprocesos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e0648-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0648-123">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="e0648-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e0648-124">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e0648-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0648-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0648-125">Requirements</span></span>



| <span data-ttu-id="e0648-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0648-126">Requirement</span></span> | <span data-ttu-id="e0648-127">Value</span><span class="sxs-lookup"><span data-stu-id="e0648-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0648-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0648-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e0648-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0648-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0648-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0648-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e0648-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0648-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0648-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0648-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0648-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0648-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

