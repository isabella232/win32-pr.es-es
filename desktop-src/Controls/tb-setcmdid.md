---
title: Mensaje de TB_SETCMDID (commctrl. h)
description: Establece el identificador de comando de un botón de la barra de herramientas.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658203"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="26b05-104">\_Mensaje SETCMDID TB</span><span class="sxs-lookup"><span data-stu-id="26b05-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="26b05-105">Establece el identificador de comando de un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="26b05-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="26b05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26b05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26b05-108">Índice de base cero del botón cuyo identificador de comando se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="26b05-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="26b05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26b05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26b05-110">Identificador del comando.</span><span class="sxs-lookup"><span data-stu-id="26b05-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b05-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b05-111">Return value</span></span>

<span data-ttu-id="26b05-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="26b05-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b05-113">Requirements</span></span>



| <span data-ttu-id="26b05-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b05-114">Requirement</span></span> | <span data-ttu-id="26b05-115">Value</span><span class="sxs-lookup"><span data-stu-id="26b05-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26b05-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b05-116">Minimum supported client</span></span><br/> | <span data-ttu-id="26b05-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26b05-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26b05-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b05-118">Minimum supported server</span></span><br/> | <span data-ttu-id="26b05-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="26b05-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26b05-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26b05-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b05-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b05-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





