---
title: Mensaje de LVM_SORTITEMSEX (commctrl. h)
description: Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la \_ macro SortItemsEx de ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078939"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="638a8-106">\_Mensaje SORTITEMSEX LVM</span><span class="sxs-lookup"><span data-stu-id="638a8-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="638a8-107">Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="638a8-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="638a8-108">El índice de cada elemento cambia para reflejar la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="638a8-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="638a8-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortItemsEx de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .</span><span class="sxs-lookup"><span data-stu-id="638a8-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="638a8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="638a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="638a8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="638a8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="638a8-112">Valor definido por la aplicación que se pasa a la función de comparación.</span><span class="sxs-lookup"><span data-stu-id="638a8-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="638a8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="638a8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="638a8-114">Puntero a una función de comparación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="638a8-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="638a8-115">Se llama a este método durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="638a8-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="638a8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="638a8-116">Return value</span></span>

<span data-ttu-id="638a8-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="638a8-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="638a8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="638a8-118">Remarks</span></span>

<span data-ttu-id="638a8-119">La función de comparación tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="638a8-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="638a8-120">Este mensaje es similar al [**LVM \_ SORTITEMS**](lvm-sortitems.md), excepto para el tipo de información que se pasa a la función de comparación.</span><span class="sxs-lookup"><span data-stu-id="638a8-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="638a8-121">Con **LVM \_ SORTITEMSEX**, *lParam1* es el índice actual del primer elemento y *lParam2* es el índice actual del segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="638a8-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="638a8-122">Puede enviar un mensaje [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) para recuperar más información sobre un elemento, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="638a8-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="638a8-123">La función de comparación debe devolver un valor negativo si el primer elemento debe preceder al segundo, un valor positivo si el primer elemento debe seguir el segundo, o cero si los dos elementos son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="638a8-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="638a8-124">Durante el proceso de ordenación, el contenido de la vista de lista es inestable.</span><span class="sxs-lookup"><span data-stu-id="638a8-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="638a8-125">Si la función de devolución de llamada envía mensajes al control de vista de lista, aparte del [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), los resultados son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="638a8-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="638a8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="638a8-126">Requirements</span></span>



| <span data-ttu-id="638a8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="638a8-127">Requirement</span></span> | <span data-ttu-id="638a8-128">Value</span><span class="sxs-lookup"><span data-stu-id="638a8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="638a8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="638a8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="638a8-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="638a8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="638a8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="638a8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="638a8-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="638a8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="638a8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="638a8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="638a8-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="638a8-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





