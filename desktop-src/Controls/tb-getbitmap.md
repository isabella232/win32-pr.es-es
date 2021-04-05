---
title: Mensaje de TB_GETBITMAP (commctrl. h)
description: Recupera el índice del mapa de bits asociado a un botón en una barra de herramientas.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- TB_GETBITMAP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997174"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="bb97b-104">\_Mensaje GETBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="bb97b-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="bb97b-105">Recupera el índice del mapa de bits asociado a un botón en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bb97b-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb97b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb97b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb97b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb97b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb97b-108">Identificador de comando del botón cuyo índice de mapa de bits se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bb97b-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="bb97b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb97b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bb97b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bb97b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb97b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb97b-111">Return value</span></span>

<span data-ttu-id="bb97b-112">Devuelve el índice del mapa de bits si se realiza correctamente o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb97b-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb97b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb97b-113">Requirements</span></span>



| <span data-ttu-id="bb97b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb97b-114">Requirement</span></span> | <span data-ttu-id="bb97b-115">Value</span><span class="sxs-lookup"><span data-stu-id="bb97b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb97b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb97b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb97b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb97b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb97b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb97b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb97b-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb97b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb97b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb97b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb97b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb97b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





