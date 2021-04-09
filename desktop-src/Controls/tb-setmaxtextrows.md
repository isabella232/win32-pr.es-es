---
title: Mensaje de TB_SETMAXTEXTROWS (commctrl. h)
description: Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996110"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="5f4c4-104">\_Mensaje SETMAXTEXTROWS TB</span><span class="sxs-lookup"><span data-stu-id="5f4c4-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="5f4c4-105">Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f4c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f4c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f4c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f4c4-108">Número máximo de filas de texto que se pueden mostrar.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5f4c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f4c4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f4c4-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4c4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f4c4-111">Return value</span></span>

<span data-ttu-id="5f4c4-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4c4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f4c4-113">Remarks</span></span>

<span data-ttu-id="5f4c4-114">Para hacer que el texto se ajuste, debe establecer el ancho máximo del botón mediante el envío de un mensaje de [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="5f4c4-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="5f4c4-115">El texto se ajusta en un salto de palabra; \\se omiten los saltos de línea ("n") en el texto.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="5f4c4-116">El texto de las \_ barras de herramientas de la lista TBSTYLE siempre se muestra en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4c4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f4c4-117">Requirements</span></span>



| <span data-ttu-id="5f4c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f4c4-118">Requirement</span></span> | <span data-ttu-id="5f4c4-119">Value</span><span class="sxs-lookup"><span data-stu-id="5f4c4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4c4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4c4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f4c4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f4c4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4c4-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f4c4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f4c4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f4c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f4c4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4c4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





