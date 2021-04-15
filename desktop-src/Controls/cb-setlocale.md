---
title: Mensaje de CB_SETLOCALE (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETLOCALE para establecer la configuración regional actual del cuadro combinado. Si el cuadro combinado tiene el \_ estilo de ordenación CBS y se agregan cadenas mediante CB \_ ADDSTRING, la configuración regional de un cuadro combinado afecta al modo en que se ordenan los elementos de la lista.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491542"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="ead59-105">Mensaje de la \_ SETLOCALE CB</span><span class="sxs-lookup"><span data-stu-id="ead59-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="ead59-106">Una aplicación envía un mensaje **CB \_ SETLOCALE** para establecer la configuración regional actual del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="ead59-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="ead59-107">Si el cuadro combinado tiene el estilo de [**\_ ordenación CBS**](combo-box-styles.md) y se agregan cadenas mediante [**CB \_ ADDSTRING**](cb-addstring.md), la configuración regional de un cuadro combinado afecta al modo en que se ordenan los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="ead59-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="ead59-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ead59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ead59-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ead59-110">Especifica el identificador de configuración regional para el cuadro combinado que se va a usar para la ordenación al agregar texto.</span><span class="sxs-lookup"><span data-stu-id="ead59-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="ead59-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ead59-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ead59-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ead59-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead59-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ead59-113">Return value</span></span>

<span data-ttu-id="ead59-114">El valor devuelto es el identificador de configuración regional anterior.</span><span class="sxs-lookup"><span data-stu-id="ead59-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="ead59-115">Si *wParam* especifica una configuración regional no instalada en el sistema, el valor devuelto es CB \_ Err y no se cambia la configuración regional del cuadro combinado actual.</span><span class="sxs-lookup"><span data-stu-id="ead59-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ead59-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ead59-116">Remarks</span></span>

<span data-ttu-id="ead59-117">Use la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir un identificador de configuración regional y la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) para construir un identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="ead59-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="ead59-118">El identificador de idioma se compone de un identificador de idioma principal y un identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="ead59-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead59-119">Requirements</span></span>



| <span data-ttu-id="ead59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead59-120">Requirement</span></span> | <span data-ttu-id="ead59-121">Value</span><span class="sxs-lookup"><span data-stu-id="ead59-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead59-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ead59-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ead59-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ead59-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ead59-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ead59-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ead59-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ead59-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead59-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ead59-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead59-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ead59-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ead59-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ead59-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ead59-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ead59-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ead59-131">**la de CB ( \_ GETLOCALE)**</span><span class="sxs-lookup"><span data-stu-id="ead59-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="ead59-132">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ead59-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ead59-133">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="ead59-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="ead59-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="ead59-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

