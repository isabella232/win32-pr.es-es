---
title: Mensaje de CB_GETCOMBOBOXINFO (Winuser. h)
description: Obtiene información sobre el cuadro combinado especificado.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489299"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="b02d4-104">\_Mensaje GETCOMBOBOXINFO CB</span><span class="sxs-lookup"><span data-stu-id="b02d4-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="b02d4-105">Obtiene información sobre el cuadro combinado especificado.</span><span class="sxs-lookup"><span data-stu-id="b02d4-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b02d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b02d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b02d4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b02d4-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b02d4-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b02d4-109">*lParam* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b02d4-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b02d4-110">Puntero a una estructura [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) que recibe la información.</span><span class="sxs-lookup"><span data-stu-id="b02d4-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02d4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b02d4-111">Return value</span></span>

<span data-ttu-id="b02d4-112">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b02d4-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="b02d4-113">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b02d4-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="b02d4-114">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b02d4-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b02d4-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b02d4-115">Remarks</span></span>

<span data-ttu-id="b02d4-116">Este mensaje es equivalente a [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="b02d4-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="b02d4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02d4-117">Requirements</span></span>



| <span data-ttu-id="b02d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02d4-118">Requirement</span></span> | <span data-ttu-id="b02d4-119">Value</span><span class="sxs-lookup"><span data-stu-id="b02d4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02d4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b02d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b02d4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b02d4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b02d4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b02d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b02d4-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b02d4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b02d4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b02d4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02d4-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b02d4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02d4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b02d4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b02d4-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b02d4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b02d4-128">**COMBOBOXINFO**</span><span class="sxs-lookup"><span data-stu-id="b02d4-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="b02d4-129">**GetComboBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="b02d4-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

