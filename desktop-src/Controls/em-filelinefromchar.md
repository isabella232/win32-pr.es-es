---
title: Mensaje de EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491224"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="5b6bf-104">\_Mensaje FILELINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="5b6bf-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="5b6bf-105">Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="5b6bf-106">Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b6bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b6bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b6bf-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b6bf-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6bf-109">Índice de carácter del carácter incluido en la línea cuyo número se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="5b6bf-110">Si este parámetro es-1, **em \_ FILELINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el símbolo de intercalación) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="5b6bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b6bf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6bf-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b6bf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b6bf-113">Return value</span></span>

<span data-ttu-id="5b6bf-114">El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam*, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5b6bf-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6bf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b6bf-115">Requirements</span></span>



| <span data-ttu-id="5b6bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6bf-116">Requirement</span></span> | <span data-ttu-id="5b6bf-117">Value</span><span class="sxs-lookup"><span data-stu-id="5b6bf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6bf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b6bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5b6bf-119">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b6bf-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b6bf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b6bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5b6bf-121">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b6bf-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b6bf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b6bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b6bf-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6bf-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b6bf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b6bf-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b6bf-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5b6bf-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b6bf-126">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="5b6bf-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





