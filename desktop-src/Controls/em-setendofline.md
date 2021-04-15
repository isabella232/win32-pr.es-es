---
title: Mensaje de EM_SETENDOFLINE (CommCtrl. h)
description: Establece el carácter de final de línea que se usa cuando se inserta un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492461"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="8f6b0-104">\_Mensaje SETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="8f6b0-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="8f6b0-105">Establece el carácter de final de línea que se usa cuando se inserta un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f6b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f6b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f6b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f6b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6b0-108">Especifica el carácter de final de línea que se usa cuando se inserta un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="8f6b0-109">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-109">This can be one of the following values.</span></span>


| <span data-ttu-id="8f6b0-110">Value</span><span class="sxs-lookup"><span data-stu-id="8f6b0-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="8f6b0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="8f6b0-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="8f6b0-112"><dt>**\_DETECTFROMCONTENT ENDOFLINE \_ EC**</dt></span><span class="sxs-lookup"><span data-stu-id="8f6b0-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="8f6b0-113">Establece el carácter de final de línea usado para New saltos en el carácter utilizado por el documento actual.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="8f6b0-114"><dt>**\_CRLF ENDOFLINE \_ EC**</dt></span><span class="sxs-lookup"><span data-stu-id="8f6b0-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="8f6b0-115">Establece el carácter de final de línea usado para New saltos en el retorno de carro seguido de avance de línea (CRLF).</span><span class="sxs-lookup"><span data-stu-id="8f6b0-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="8f6b0-116"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="8f6b0-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="8f6b0-117">Establece el carácter de final de línea usado para New saltos en el retorno de carro (CR).</span><span class="sxs-lookup"><span data-stu-id="8f6b0-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="8f6b0-118"><dt>**\_ENDOFLINE de \_ LF de EC**</dt></span><span class="sxs-lookup"><span data-stu-id="8f6b0-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="8f6b0-119">Establece el carácter de final de línea usado para New saltos en avance de línea (LF).</span><span class="sxs-lookup"><span data-stu-id="8f6b0-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="8f6b0-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f6b0-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6b0-121">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f6b0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f6b0-122">Return value</span></span>

<span data-ttu-id="8f6b0-123">Si la operación se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="8f6b0-124">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8f6b0-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f6b0-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f6b0-125">Remarks</span></span>

<span data-ttu-id="8f6b0-126">Cuando el juego de caracteres de fin de línea es **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, el control de edición solo detectará los caracteres de fin de línea admitidos según su estilo de ventana extendido, vea [Editar estilos extendidos del control](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8f6b0-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6b0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f6b0-127">Requirements</span></span>



| <span data-ttu-id="8f6b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f6b0-128">Requirement</span></span> | <span data-ttu-id="8f6b0-129">Value</span><span class="sxs-lookup"><span data-stu-id="8f6b0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6b0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f6b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6b0-131">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f6b0-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f6b0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f6b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6b0-133">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f6b0-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f6b0-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f6b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f6b0-135"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f6b0-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6b0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f6b0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6b0-137">\**\_GETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="8f6b0-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





