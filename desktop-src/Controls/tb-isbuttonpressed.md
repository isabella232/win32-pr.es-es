---
title: Mensaje de TB_ISBUTTONPRESSED (commctrl. h)
description: Determina si se presiona el botón especificado en una barra de herramientas.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150066"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="f2b41-104">\_Mensaje ISBUTTONPRESSED TB</span><span class="sxs-lookup"><span data-stu-id="f2b41-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="f2b41-105">Determina si se presiona el botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f2b41-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2b41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2b41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2b41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2b41-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="f2b41-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="f2b41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2b41-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2b41-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2b41-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b41-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2b41-111">Return value</span></span>

<span data-ttu-id="f2b41-112">Devuelve un valor distinto de cero si el botón está presionado o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f2b41-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b41-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2b41-113">Requirements</span></span>



| <span data-ttu-id="f2b41-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2b41-114">Requirement</span></span> | <span data-ttu-id="f2b41-115">Value</span><span class="sxs-lookup"><span data-stu-id="f2b41-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b41-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2b41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b41-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2b41-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2b41-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2b41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b41-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2b41-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2b41-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2b41-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b41-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b41-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





