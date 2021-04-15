---
title: Mensaje de EM_FILELINELENGTH (CommCtrl. h)
description: Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534371"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="317e4-104">\_Mensaje FILELINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="317e4-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="317e4-105">Recupera la longitud, en caracteres, de una línea en un control de edición, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="317e4-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="317e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="317e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="317e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="317e4-108">Índice de carácter de un carácter de la línea cuya longitud se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="317e4-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="317e4-109">Si este parámetro es mayor que el número de caracteres del control, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="317e4-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="317e4-110">Este parámetro puede ser-1.</span><span class="sxs-lookup"><span data-stu-id="317e4-110">This parameter can be -1.</span></span> <span data-ttu-id="317e4-111">En este caso, el mensaje devuelve el número de caracteres no seleccionados en líneas que contienen los caracteres seleccionados.</span><span class="sxs-lookup"><span data-stu-id="317e4-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="317e4-112">Por ejemplo, si la selección se extiende desde el cuarto carácter de una línea hasta el octavo carácter desde el final de la línea siguiente, el valor devuelto sería 10 (tres caracteres en la primera línea y siete en el siguiente).</span><span class="sxs-lookup"><span data-stu-id="317e4-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="317e4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="317e4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="317e4-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="317e4-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317e4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="317e4-115">Return value</span></span>

<span data-ttu-id="317e4-116">En el caso de los controles de edición multilínea, el valor devuelto es la longitud, en **TCHAR** s, de la línea especificada por el parámetro *wParam* , independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="317e4-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="317e4-117">No incluye el carácter de retorno de carro o avance de línea al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="317e4-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="317e4-118">En el caso de los controles de edición de una sola línea, el valor devuelto es la longitud, en **TCHAR** s, del texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="317e4-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="317e4-119">Si *wParam* es mayor que el número de caracteres del control, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="317e4-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="317e4-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="317e4-120">Remarks</span></span>

<span data-ttu-id="317e4-121">Use el [**mensaje \_ FILELINEINDEX em**](em-lineindex.md) para recuperar un índice de carácter para un número de línea determinado dentro de un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="317e4-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="317e4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="317e4-122">Requirements</span></span>



| <span data-ttu-id="317e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="317e4-123">Requirement</span></span> | <span data-ttu-id="317e4-124">Value</span><span class="sxs-lookup"><span data-stu-id="317e4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="317e4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="317e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="317e4-126">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="317e4-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="317e4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="317e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="317e4-128">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="317e4-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="317e4-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="317e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="317e4-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="317e4-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317e4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="317e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317e4-132">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="317e4-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





