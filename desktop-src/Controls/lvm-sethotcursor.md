---
title: Mensaje de LVM_SETHOTCURSOR (commctrl. h)
description: Establece el valor de HCURSOR que usa el control de vista de lista cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801111"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="2cffe-104">\_Mensaje SETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="2cffe-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="2cffe-105">Establece el valor de HCURSOR que usa el control de vista de lista cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo.</span><span class="sxs-lookup"><span data-stu-id="2cffe-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="2cffe-106">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetHotCursor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="2cffe-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="2cffe-107">Para comprobar si el seguimiento activo está habilitado, llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="2cffe-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="2cffe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cffe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cffe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cffe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2cffe-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2cffe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2cffe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cffe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cffe-112">Identificador del cursor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="2cffe-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cffe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cffe-113">Return value</span></span>

<span data-ttu-id="2cffe-114">Devuelve un valor de HCURSOR que es el cursor activo anterior.</span><span class="sxs-lookup"><span data-stu-id="2cffe-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cffe-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cffe-115">Remarks</span></span>

<span data-ttu-id="2cffe-116">Un control de vista de lista usa el seguimiento activo y la selección del mouse cuando se establece el estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2cffe-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cffe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cffe-117">Requirements</span></span>



| <span data-ttu-id="2cffe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cffe-118">Requirement</span></span> | <span data-ttu-id="2cffe-119">Value</span><span class="sxs-lookup"><span data-stu-id="2cffe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cffe-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cffe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2cffe-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2cffe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2cffe-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cffe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2cffe-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cffe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2cffe-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cffe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cffe-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cffe-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

