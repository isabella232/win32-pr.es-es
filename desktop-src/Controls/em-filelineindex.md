---
title: Mensaje de EM_FILELINEINDEX (CommCtrl. h)
description: Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150468"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="1f307-104">Mensaje de EM_FILELINEINDEX (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="1f307-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="1f307-105">Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1f307-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="1f307-106">Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.</span><span class="sxs-lookup"><span data-stu-id="1f307-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f307-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f307-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f307-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f307-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f307-109">Número de línea de base cero.</span><span class="sxs-lookup"><span data-stu-id="1f307-109">The zero-based line number.</span></span> <span data-ttu-id="1f307-110">Un valor de-1 especifica el número de línea actual (la línea que contiene el símbolo de intercalación).</span><span class="sxs-lookup"><span data-stu-id="1f307-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="1f307-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f307-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f307-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1f307-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f307-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f307-113">Return value</span></span>

<span data-ttu-id="1f307-114">El valor devuelto es el índice de carácter de la línea especificada en el parámetro *wParam* , independientemente de cómo se muestran las líneas en la pantalla o es-1 si el número de línea especificado es mayor que el número de líneas del control de edición.</span><span class="sxs-lookup"><span data-stu-id="1f307-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f307-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f307-115">Requirements</span></span>



| <span data-ttu-id="1f307-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f307-116">Requirement</span></span> | <span data-ttu-id="1f307-117">Value</span><span class="sxs-lookup"><span data-stu-id="1f307-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f307-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f307-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f307-119">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f307-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1f307-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f307-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f307-121">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f307-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f307-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f307-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f307-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f307-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f307-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f307-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f307-125">**\_FILELINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="1f307-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





