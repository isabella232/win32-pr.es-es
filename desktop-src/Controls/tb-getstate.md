---
title: Mensaje de TB_GETSTATE (commctrl. h)
description: Recupera información sobre el estado del botón especificado en una barra de herramientas, como, por ejemplo, si está habilitado, presionado o activado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905081"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="09fbf-104">\_Mensaje GETSTATE TB</span><span class="sxs-lookup"><span data-stu-id="09fbf-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="09fbf-105">Recupera información sobre el estado del botón especificado en una barra de herramientas, como, por ejemplo, si está habilitado, presionado o activado.</span><span class="sxs-lookup"><span data-stu-id="09fbf-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="09fbf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fbf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09fbf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09fbf-108">Identificador de comando del botón para el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="09fbf-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="09fbf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09fbf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="09fbf-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="09fbf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fbf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09fbf-111">Return value</span></span>

<span data-ttu-id="09fbf-112">Devuelve la información de estado del botón si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="09fbf-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="09fbf-113">La información sobre el estado de los botones puede ser una combinación de los valores que aparecen en [**los Estados**](toolbar-button-states.md)de los botones de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="09fbf-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09fbf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fbf-114">Requirements</span></span>



| <span data-ttu-id="09fbf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fbf-115">Requirement</span></span> | <span data-ttu-id="09fbf-116">Value</span><span class="sxs-lookup"><span data-stu-id="09fbf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09fbf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09fbf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09fbf-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09fbf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09fbf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09fbf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09fbf-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09fbf-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09fbf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09fbf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fbf-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fbf-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





