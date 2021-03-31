---
title: Mensaje de LB_SETLOCALE (Winuser. h)
description: Establece la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el \_ estilo de ordenación lbs) y del texto agregado por el mensaje de lb en lb \_ .
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079656"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="0b144-105">Mensaje de LB \_ SETLOCALE</span><span class="sxs-lookup"><span data-stu-id="0b144-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="0b144-106">Establece la configuración regional actual del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="0b144-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="0b144-107">Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) ) y del texto agregado por el mensaje de [**lb en lb \_**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="0b144-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b144-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b144-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b144-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b144-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b144-110">Especifica el identificador de configuración regional que el cuadro de lista usará para la ordenación al agregar texto.</span><span class="sxs-lookup"><span data-stu-id="0b144-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="0b144-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b144-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b144-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0b144-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b144-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b144-113">Return value</span></span>

<span data-ttu-id="0b144-114">El valor devuelto es el identificador de configuración regional anterior.</span><span class="sxs-lookup"><span data-stu-id="0b144-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="0b144-115">Si el parámetro *wParam* especifica una configuración regional que no está instalada en el sistema, el valor devuelto es lb \_ Err y la configuración regional del cuadro de lista actual no cambia.</span><span class="sxs-lookup"><span data-stu-id="0b144-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b144-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b144-116">Remarks</span></span>

<span data-ttu-id="0b144-117">Use la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="0b144-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b144-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b144-118">Requirements</span></span>



| <span data-ttu-id="0b144-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b144-119">Requirement</span></span> | <span data-ttu-id="0b144-120">Value</span><span class="sxs-lookup"><span data-stu-id="0b144-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b144-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b144-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b144-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0b144-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b144-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b144-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b144-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b144-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b144-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b144-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b144-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b144-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b144-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b144-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b144-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0b144-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b144-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="0b144-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="0b144-130">**equilibro \_ de lb**</span><span class="sxs-lookup"><span data-stu-id="0b144-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

