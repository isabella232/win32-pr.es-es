---
title: TVM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TVM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control.'
ms.assetid: e4b58ae5-6217-4a2e-80e5-3ba9e578859a
keywords:
- TVM_SETUNICODEFORMAT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- TVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fcdd22cff0ac91885ef8f54d49922f9c677e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116553"
---
# <a name="tvm_setunicodeformat-message"></a><span data-ttu-id="87d31-104">Mensaje \_ SETUNICODEFORMAT de TVM</span><span class="sxs-lookup"><span data-stu-id="87d31-104">TVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="87d31-105">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="87d31-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="87d31-106">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="87d31-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="87d31-107">Puede enviar este mensaje explícitamente o usar la macro [**\_ SetUnicodeFormat de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat)</span><span class="sxs-lookup"><span data-stu-id="87d31-107">You can send this message explicitly or use the [**TreeView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87d31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87d31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87d31-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87d31-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="87d31-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="87d31-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="87d31-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="87d31-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="87d31-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="87d31-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87d31-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87d31-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="87d31-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d31-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87d31-115">Return value</span></span>

<span data-ttu-id="87d31-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="87d31-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d31-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87d31-117">Remarks</span></span>

<span data-ttu-id="87d31-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="87d31-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d31-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87d31-119">Requirements</span></span>



| <span data-ttu-id="87d31-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d31-120">Requirement</span></span> | <span data-ttu-id="87d31-121">Valor</span><span class="sxs-lookup"><span data-stu-id="87d31-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87d31-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87d31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="87d31-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="87d31-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87d31-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87d31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="87d31-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="87d31-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87d31-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87d31-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d31-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="87d31-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d31-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="87d31-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d31-129">**TVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="87d31-129">**TVM\_GETUNICODEFORMAT**</span></span>](tvm-getunicodeformat.md)
</dt> </dl>

 

 





