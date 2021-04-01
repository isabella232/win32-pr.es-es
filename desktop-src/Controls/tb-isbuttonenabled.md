---
title: Mensaje de TB_ISBUTTONENABLED (commctrl. h)
description: Determina si el botón especificado de una barra de herramientas está habilitado.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905132"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="5fcce-104">\_Mensaje ISBUTTONENABLED TB</span><span class="sxs-lookup"><span data-stu-id="5fcce-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="5fcce-105">Determina si el botón especificado de una barra de herramientas está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5fcce-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fcce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fcce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fcce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fcce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fcce-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="5fcce-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="5fcce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fcce-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5fcce-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5fcce-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fcce-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fcce-111">Return value</span></span>

<span data-ttu-id="5fcce-112">Devuelve un valor distinto de cero si el botón está habilitado o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5fcce-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fcce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fcce-113">Requirements</span></span>



| <span data-ttu-id="5fcce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fcce-114">Requirement</span></span> | <span data-ttu-id="5fcce-115">Value</span><span class="sxs-lookup"><span data-stu-id="5fcce-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcce-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fcce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fcce-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5fcce-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fcce-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fcce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fcce-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5fcce-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fcce-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fcce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fcce-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fcce-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





