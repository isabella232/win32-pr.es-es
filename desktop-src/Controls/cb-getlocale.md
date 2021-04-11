---
title: Mensaje de CB_GETLOCALE (Winuser. h)
description: Obtiene la configuración regional actual del cuadro combinado. La configuración regional se usa para determinar el criterio de ordenación correcto del texto que se muestra en los cuadros combinados con el \_ estilo de ordenación CBS y el texto agregado mediante el \_ mensaje CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079363"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="ce67d-105">Mensaje de error de CB. \_</span><span class="sxs-lookup"><span data-stu-id="ce67d-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="ce67d-106">Obtiene la configuración regional actual del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="ce67d-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="ce67d-107">La configuración regional se usa para determinar el criterio de ordenación correcto del texto que se muestra en los cuadros combinados con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) y el texto agregado mediante el mensaje [**CB \_ ADDSTRING**](cb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="ce67d-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce67d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce67d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce67d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce67d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce67d-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ce67d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce67d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce67d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce67d-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ce67d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce67d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce67d-113">Return value</span></span>

<span data-ttu-id="ce67d-114">El valor devuelto especifica la configuración regional actual del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="ce67d-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="ce67d-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el código de país o región y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="ce67d-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce67d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce67d-116">Remarks</span></span>

<span data-ttu-id="ce67d-117">El identificador de idioma se compone de un identificador de subidioma y un identificador de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="ce67d-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="ce67d-118">La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) obtiene el identificador de idioma principal y la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) obtiene el identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="ce67d-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce67d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce67d-119">Requirements</span></span>



| <span data-ttu-id="ce67d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce67d-120">Requirement</span></span> | <span data-ttu-id="ce67d-121">Value</span><span class="sxs-lookup"><span data-stu-id="ce67d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce67d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce67d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce67d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce67d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ce67d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce67d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce67d-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce67d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce67d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce67d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce67d-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce67d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce67d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce67d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce67d-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ce67d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce67d-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ce67d-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ce67d-131">**CB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="ce67d-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="ce67d-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ce67d-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ce67d-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce67d-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ce67d-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce67d-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ce67d-135">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="ce67d-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="ce67d-136">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="ce67d-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

