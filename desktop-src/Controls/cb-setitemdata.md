---
title: Mensaje de CB_SETITEMDATA (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETITEMDATA para establecer el valor asociado al elemento especificado en un cuadro combinado.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905408"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="91304-104">\_Mensaje SETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="91304-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="91304-105">Una aplicación envía un mensaje **CB \_ SETITEMDATA** para establecer el valor asociado al elemento especificado en un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="91304-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="91304-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91304-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91304-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91304-108">Especifica el índice basado en cero del elemento.</span><span class="sxs-lookup"><span data-stu-id="91304-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="91304-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91304-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91304-110">Especifica el nuevo valor que se va a asociar al elemento.</span><span class="sxs-lookup"><span data-stu-id="91304-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91304-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91304-111">Return value</span></span>

<span data-ttu-id="91304-112">Si se produce un error, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="91304-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="91304-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91304-113">Remarks</span></span>

<span data-ttu-id="91304-114">Si el elemento especificado se encuentra en un cuadro combinado dibujado por el propietario creado sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , este mensaje reemplaza el valor del parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) que agregó el elemento al cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="91304-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="91304-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91304-115">Requirements</span></span>



| <span data-ttu-id="91304-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91304-116">Requirement</span></span> | <span data-ttu-id="91304-117">Value</span><span class="sxs-lookup"><span data-stu-id="91304-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91304-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91304-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91304-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91304-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91304-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91304-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91304-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91304-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91304-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91304-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91304-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91304-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91304-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="91304-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="91304-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="91304-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91304-126">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="91304-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="91304-127">**CB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="91304-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="91304-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="91304-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





