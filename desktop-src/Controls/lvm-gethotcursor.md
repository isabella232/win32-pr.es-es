---
title: Mensaje de LVM_GETHOTCURSOR (commctrl. h)
description: Recupera el valor de HCURSOR que se usa cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHotCursor de ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803404"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="472be-105">\_Mensaje GETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="472be-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="472be-106">Recupera el valor de HCURSOR que se usa cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo.</span><span class="sxs-lookup"><span data-stu-id="472be-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="472be-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHotCursor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="472be-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="472be-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="472be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="472be-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="472be-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="472be-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="472be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="472be-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="472be-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="472be-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="472be-113">Return value</span></span>

<span data-ttu-id="472be-114">Devuelve un valor de HCURSOR que es el identificador del cursor que el control de vista de lista utiliza cuando está habilitado el seguimiento activo.</span><span class="sxs-lookup"><span data-stu-id="472be-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="472be-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="472be-115">Remarks</span></span>

<span data-ttu-id="472be-116">Un control de vista de lista usa el seguimiento activo y la selección del mouse cuando se establece el estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="472be-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="472be-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472be-117">Requirements</span></span>



| <span data-ttu-id="472be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="472be-118">Requirement</span></span> | <span data-ttu-id="472be-119">Value</span><span class="sxs-lookup"><span data-stu-id="472be-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="472be-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="472be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="472be-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="472be-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="472be-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="472be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="472be-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="472be-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="472be-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="472be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="472be-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="472be-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





