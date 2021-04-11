---
title: Mensaje de TB_SETSTATE (commctrl. h)
description: Establece el estado del botón especificado en una barra de herramientas.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151255"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="f5d8a-104">Mensaje de TB \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="f5d8a-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="f5d8a-105">Establece el estado del botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f5d8a-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5d8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5d8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d8a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5d8a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5d8a-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="f5d8a-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="f5d8a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5d8a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5d8a-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es una combinación de los valores que aparecen en [los Estados de los botones](toolbar-button-states.md)de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f5d8a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="f5d8a-111">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f5d8a-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d8a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d8a-112">Return value</span></span>

<span data-ttu-id="f5d8a-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f5d8a-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d8a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d8a-114">Requirements</span></span>



| <span data-ttu-id="f5d8a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d8a-115">Requirement</span></span> | <span data-ttu-id="f5d8a-116">Value</span><span class="sxs-lookup"><span data-stu-id="f5d8a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d8a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d8a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d8a-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5d8a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5d8a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d8a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d8a-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5d8a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5d8a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5d8a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d8a-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d8a-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

