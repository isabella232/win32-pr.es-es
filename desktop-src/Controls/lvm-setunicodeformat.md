---
title: Mensaje de LVM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- LVM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b1e29d933892a24d7bc2ab472c7d591375362a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658328"
---
# <a name="lvm_setunicodeformat-message"></a><span data-ttu-id="c6d9b-104">\_Mensaje SETUNICODEFORMAT LVM</span><span class="sxs-lookup"><span data-stu-id="c6d9b-104">LVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="c6d9b-105">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="c6d9b-106">Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="c6d9b-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetUnicodeFormat de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="c6d9b-107">You can send this message explicitly or use the [**ListView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6d9b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6d9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6d9b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d9b-110">Determina el juego de caracteres utilizado por el control.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="c6d9b-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="c6d9b-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="c6d9b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6d9b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c6d9b-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6d9b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6d9b-115">Return value</span></span>

<span data-ttu-id="c6d9b-116">Devuelve la marca de formato Unicode anterior para el control.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d9b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6d9b-117">Remarks</span></span>

<span data-ttu-id="c6d9b-118">Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6d9b-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d9b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6d9b-119">Requirements</span></span>



| <span data-ttu-id="c6d9b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d9b-120">Requirement</span></span> | <span data-ttu-id="c6d9b-121">Value</span><span class="sxs-lookup"><span data-stu-id="c6d9b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d9b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6d9b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d9b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6d9b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6d9b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6d9b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d9b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6d9b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6d9b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6d9b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d9b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6d9b-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d9b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6d9b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d9b-129">**\_GETUNICODEFORMAT LVM**</span><span class="sxs-lookup"><span data-stu-id="c6d9b-129">**LVM\_GETUNICODEFORMAT**</span></span>](lvm-getunicodeformat.md)
</dt> </dl>

 

 





