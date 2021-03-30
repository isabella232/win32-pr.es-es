---
title: Mensaje de TB_GETBUTTON (commctrl. h)
description: Recupera información sobre el botón especificado en una barra de herramientas.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804123"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="c9558-104">\_Mensaje GETBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="c9558-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="c9558-105">Recupera información sobre el botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="c9558-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9558-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9558-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9558-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9558-108">Índice de base cero del botón para el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="c9558-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="c9558-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9558-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9558-110">Puntero a la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que recibe la información del botón.</span><span class="sxs-lookup"><span data-stu-id="c9558-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9558-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9558-111">Return value</span></span>

<span data-ttu-id="c9558-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c9558-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9558-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9558-113">Requirements</span></span>



| <span data-ttu-id="c9558-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9558-114">Requirement</span></span> | <span data-ttu-id="c9558-115">Value</span><span class="sxs-lookup"><span data-stu-id="c9558-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9558-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9558-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9558-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9558-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9558-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9558-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9558-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9558-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9558-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9558-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9558-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9558-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





