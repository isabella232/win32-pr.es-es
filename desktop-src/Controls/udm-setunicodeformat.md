---
title: Mensaje de UDM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- UDM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3f9dbc1e19fdb43aa0b7d5e6de6fdddd308eb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079426"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="35ed9-105">\_Mensaje SETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="35ed9-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="35ed9-106">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="35ed9-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="35ed9-107">Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="35ed9-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="35ed9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35ed9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ed9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35ed9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ed9-110">Determina el juego de caracteres utilizado por el control.</span><span class="sxs-lookup"><span data-stu-id="35ed9-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="35ed9-111">Si este valor es **true**, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="35ed9-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="35ed9-112">Si este valor es **false**, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="35ed9-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="35ed9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35ed9-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="35ed9-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35ed9-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ed9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35ed9-115">Return value</span></span>

<span data-ttu-id="35ed9-116">Devuelve la marca de formato Unicode anterior para el control.</span><span class="sxs-lookup"><span data-stu-id="35ed9-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ed9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35ed9-117">Remarks</span></span>

<span data-ttu-id="35ed9-118">Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="35ed9-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ed9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ed9-119">Requirements</span></span>



| <span data-ttu-id="35ed9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ed9-120">Requirement</span></span> | <span data-ttu-id="35ed9-121">Value</span><span class="sxs-lookup"><span data-stu-id="35ed9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ed9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35ed9-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="35ed9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35ed9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ed9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35ed9-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="35ed9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35ed9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35ed9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ed9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ed9-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ed9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ed9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ed9-129">**UDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="35ed9-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





