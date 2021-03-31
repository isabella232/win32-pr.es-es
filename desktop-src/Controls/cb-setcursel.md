---
title: Mensaje de CB_SETCURSEL (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETCURSEL para seleccionar una cadena en la lista de un cuadro combinado.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079355"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="7b4b0-104">\_Mensaje SETCURSEL CB</span><span class="sxs-lookup"><span data-stu-id="7b4b0-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="7b4b0-105">Una aplicación envía un mensaje **CB \_ SETCURSEL** para seleccionar una cadena en la lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="7b4b0-106">Si es necesario, la lista desplaza la cadena a la vista.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="7b4b0-107">El texto del control de edición del cuadro combinado cambia para reflejar la nueva selección, y se quita cualquier selección anterior en la lista.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b4b0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b4b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b4b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b4b0-110">Especifica el índice de base cero de la cadena que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="7b4b0-111">Si este parámetro es-1, se quita cualquier selección actual de la lista y se borra el control de edición.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="7b4b0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b4b0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b4b0-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4b0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b4b0-114">Return value</span></span>

<span data-ttu-id="7b4b0-115">Si el mensaje se realiza correctamente, el valor devuelto es el índice del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="7b4b0-116">Si *wParam* es mayor que el número de elementos de la lista o si *wParam* es-1, el valor devuelto es CB \_ Err y se borra la selección.</span><span class="sxs-lookup"><span data-stu-id="7b4b0-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4b0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b4b0-117">Requirements</span></span>



| <span data-ttu-id="7b4b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4b0-118">Requirement</span></span> | <span data-ttu-id="7b4b0-119">Value</span><span class="sxs-lookup"><span data-stu-id="7b4b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4b0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b4b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4b0-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7b4b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b4b0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b4b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4b0-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b4b0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b4b0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b4b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b4b0-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b4b0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4b0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b4b0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b4b0-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7b4b0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7b4b0-128">**CB \_ FINDSTRING**</span><span class="sxs-lookup"><span data-stu-id="7b4b0-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="7b4b0-129">**CB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="7b4b0-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="7b4b0-130">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="7b4b0-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





