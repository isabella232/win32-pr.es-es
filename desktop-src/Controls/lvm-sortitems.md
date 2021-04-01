---
title: Mensaje de LVM_SORTITEMS (commctrl. h)
description: Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la \_ macro SortItems de ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997189"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="979c7-106">\_Mensaje SORTITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="979c7-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="979c7-107">Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="979c7-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="979c7-108">El índice de cada elemento cambia para reflejar la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="979c7-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="979c7-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .</span><span class="sxs-lookup"><span data-stu-id="979c7-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="979c7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="979c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979c7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="979c7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="979c7-112">Valor definido por la aplicación que se pasa a la función de comparación.</span><span class="sxs-lookup"><span data-stu-id="979c7-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="979c7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="979c7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="979c7-114">Puntero a la función de comparación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="979c7-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="979c7-115">La función de comparación se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.</span><span class="sxs-lookup"><span data-stu-id="979c7-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979c7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="979c7-116">Return value</span></span>

<span data-ttu-id="979c7-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="979c7-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="979c7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="979c7-118">Remarks</span></span>

<span data-ttu-id="979c7-119">La función de comparación tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="979c7-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="979c7-120">El parámetro *lParam1* es el valor asociado al primer elemento que se está comparando y el parámetro *lParam2* es el valor asociado al segundo elemento.</span><span class="sxs-lookup"><span data-stu-id="979c7-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="979c7-121">Estos son los valores que se especificaron en el miembro **lParam** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de los elementos cuando se insertaron en la lista.</span><span class="sxs-lookup"><span data-stu-id="979c7-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="979c7-122">El parámetro *wParam* de [**\_ SortItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)se pasa a la función de devolución de llamada como tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="979c7-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="979c7-123">La función de comparación debe devolver un valor negativo si el primer elemento debe preceder al segundo, un valor positivo si el primer elemento debe seguir el segundo, o cero si los dos elementos son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="979c7-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="979c7-124">Durante el proceso de ordenación, el contenido de la vista de lista es inestable.</span><span class="sxs-lookup"><span data-stu-id="979c7-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="979c7-125">Si la función de devolución de llamada envía mensajes al control de vista de lista, aparte del [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), los resultados son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="979c7-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="979c7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="979c7-126">Requirements</span></span>



| <span data-ttu-id="979c7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="979c7-127">Requirement</span></span> | <span data-ttu-id="979c7-128">Value</span><span class="sxs-lookup"><span data-stu-id="979c7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="979c7-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="979c7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="979c7-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="979c7-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="979c7-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="979c7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="979c7-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="979c7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="979c7-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="979c7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="979c7-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="979c7-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





