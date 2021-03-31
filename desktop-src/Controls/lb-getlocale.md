---
title: Mensaje de LB_GETLOCALE (Winuser. h)
description: Obtiene la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el \_ estilo de ordenación lbs) y del texto agregado por el mensaje de lb en lb \_ .
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491182"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="59b81-105">Mensaje de LB. \_</span><span class="sxs-lookup"><span data-stu-id="59b81-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="59b81-106">Obtiene la configuración regional actual del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="59b81-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="59b81-107">Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) ) y del texto agregado por el mensaje de [**lb en lb \_**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="59b81-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="59b81-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b81-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59b81-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b81-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="59b81-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="59b81-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59b81-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59b81-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="59b81-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b81-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b81-113">Return value</span></span>

<span data-ttu-id="59b81-114">El valor devuelto especifica la configuración regional actual del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="59b81-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="59b81-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el código de país o región y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="59b81-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b81-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59b81-116">Remarks</span></span>

<span data-ttu-id="59b81-117">El identificador de idioma está formado por un identificador de subidioma y un identificador de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="59b81-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="59b81-118">Use la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) para extraer el identificador de idioma principal del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valor devuelto y la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) para extraer el identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="59b81-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b81-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b81-119">Requirements</span></span>



| <span data-ttu-id="59b81-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b81-120">Requirement</span></span> | <span data-ttu-id="59b81-121">Value</span><span class="sxs-lookup"><span data-stu-id="59b81-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b81-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b81-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59b81-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59b81-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59b81-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b81-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59b81-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="59b81-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59b81-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59b81-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b81-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59b81-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b81-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b81-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="59b81-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="59b81-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59b81-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="59b81-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="59b81-131">**LB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="59b81-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="59b81-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="59b81-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="59b81-133">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="59b81-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="59b81-134">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="59b81-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

