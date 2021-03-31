---
title: Mensaje de CB_LIMITTEXT (Winuser. h)
description: Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079359"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="52871-104">\_Mensaje LIMITTEXT CB</span><span class="sxs-lookup"><span data-stu-id="52871-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="52871-105">Limita la longitud del texto que el usuario puede escribir en el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="52871-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="52871-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52871-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52871-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52871-108">Número máximo de **TCHARs** que puede escribir el usuario, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="52871-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="52871-109">Si este parámetro es cero, la longitud del texto se limita a caracteres 0x7FFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="52871-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="52871-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52871-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52871-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="52871-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52871-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52871-112">Return value</span></span>

<span data-ttu-id="52871-113">El valor devuelto siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="52871-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="52871-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52871-114">Remarks</span></span>

<span data-ttu-id="52871-115">Si el cuadro combinado no tiene el estilo [**\_ AUTOHSCROLL de CBS**](combo-box-styles.md) , establecer el límite de texto en un valor mayor que el tamaño del control de edición no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="52871-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="52871-116">El mensaje **CB \_ LIMITTEXT** limita solo el texto que el usuario puede escribir.</span><span class="sxs-lookup"><span data-stu-id="52871-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="52871-117">No tiene ningún efecto en ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición cuando se selecciona una cadena en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="52871-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="52871-118">El límite predeterminado para el texto que un usuario puede escribir en el control de edición es 30.000 **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="52871-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52871-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52871-119">Requirements</span></span>



| <span data-ttu-id="52871-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="52871-120">Requirement</span></span> | <span data-ttu-id="52871-121">Value</span><span class="sxs-lookup"><span data-stu-id="52871-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52871-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52871-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52871-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52871-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52871-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52871-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52871-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="52871-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52871-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52871-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52871-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52871-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





