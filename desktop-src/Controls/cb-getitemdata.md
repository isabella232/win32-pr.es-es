---
title: Mensaje de CB_GETITEMDATA (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETITEMDATA a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado en el cuadro combinado.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802240"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="e4331-104">\_Mensaje GETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="e4331-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="e4331-105">Una aplicación envía un mensaje **CB \_ GETITEMDATA** a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado en el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e4331-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4331-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4331-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4331-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4331-108">El índice de base cero de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e4331-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="e4331-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4331-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4331-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e4331-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4331-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4331-111">Return value</span></span>

<span data-ttu-id="e4331-112">El valor devuelto es el valor asociado al elemento.</span><span class="sxs-lookup"><span data-stu-id="e4331-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="e4331-113">Si se produce un error, es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="e4331-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="e4331-114">Si el elemento está en un cuadro combinado dibujado por el propietario creado sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor devuelto es el valor contenido en el parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) , que agregó el elemento al cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e4331-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="e4331-115">Si no se usó el estilo **CBS \_ HASSTRINGS** , el valor devuelto es el parámetro *lParam* contenido en un mensaje [**\_ SETITEMDATA de CB**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e4331-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4331-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4331-116">Requirements</span></span>



| <span data-ttu-id="e4331-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4331-117">Requirement</span></span> | <span data-ttu-id="e4331-118">Value</span><span class="sxs-lookup"><span data-stu-id="e4331-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4331-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4331-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4331-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4331-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4331-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4331-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4331-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4331-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4331-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4331-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4331-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4331-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4331-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4331-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4331-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e4331-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4331-127">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="e4331-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e4331-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="e4331-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="e4331-129">**CB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="e4331-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





