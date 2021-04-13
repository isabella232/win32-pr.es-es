---
title: Mensaje de SB_SETTIPTEXT (commctrl. h)
description: Establece el texto de información sobre herramientas para un elemento de una barra de estado. La barra de estado se debe haber creado con el \_ estilo de información sobre herramientas de SBT para habilitar la información sobre herramientas.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491987"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="f4418-105">\_Mensaje SETTIPTEXT de SB</span><span class="sxs-lookup"><span data-stu-id="f4418-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="f4418-106">Establece el texto de información sobre herramientas para un elemento de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="f4418-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="f4418-107">La barra de estado se debe haber creado con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f4418-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4418-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4418-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4418-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4418-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4418-110">Índice de base cero del elemento que recibirá el texto de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f4418-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="f4418-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4418-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4418-112">Puntero a un búfer de caracteres que contiene el nuevo texto de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f4418-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4418-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4418-113">Return value</span></span>

<span data-ttu-id="f4418-114">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f4418-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4418-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4418-115">Remarks</span></span>

<span data-ttu-id="f4418-116">Este texto de información sobre herramientas se muestra en dos situaciones:</span><span class="sxs-lookup"><span data-stu-id="f4418-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="f4418-117">Cuando el panel correspondiente de la barra de estado solo contiene un icono.</span><span class="sxs-lookup"><span data-stu-id="f4418-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="f4418-118">Cuando el panel correspondiente de la barra de estado contiene texto truncado debido al tamaño del panel.</span><span class="sxs-lookup"><span data-stu-id="f4418-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4418-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4418-119">Requirements</span></span>



| <span data-ttu-id="f4418-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4418-120">Requirement</span></span> | <span data-ttu-id="f4418-121">Value</span><span class="sxs-lookup"><span data-stu-id="f4418-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4418-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4418-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4418-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4418-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4418-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4418-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4418-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4418-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4418-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4418-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4418-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4418-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f4418-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f4418-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4418-129">**SB \_ SETTIPTEXTW** (Unicode) y **SB \_ SETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4418-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





