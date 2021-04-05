---
title: Mensaje de TB_MAPACCELERATOR (commctrl. h)
description: Determina el identificador del botón que corresponde al carácter de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803145"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="bf379-104">\_Mensaje MAPACCELERATOR TB</span><span class="sxs-lookup"><span data-stu-id="bf379-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="bf379-105">Determina el identificador del botón que corresponde al carácter de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="bf379-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf379-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf379-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf379-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf379-108">Carácter de acelerador.</span><span class="sxs-lookup"><span data-stu-id="bf379-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="bf379-109">*lParam* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bf379-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf379-110">Puntero a un **uint**.</span><span class="sxs-lookup"><span data-stu-id="bf379-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="bf379-111">En la devolución, si se realiza correctamente, este parámetro contendrá el identificador del botón que tiene *wParam* como carácter de aceleración.</span><span class="sxs-lookup"><span data-stu-id="bf379-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf379-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf379-112">Return value</span></span>

<span data-ttu-id="bf379-113">Devuelve un valor distinto de cero si uno de los botones tiene *wParam* como carácter de acelerador o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bf379-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf379-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf379-114">Requirements</span></span>



| <span data-ttu-id="bf379-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf379-115">Requirement</span></span> | <span data-ttu-id="bf379-116">Value</span><span class="sxs-lookup"><span data-stu-id="bf379-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf379-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf379-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf379-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bf379-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf379-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf379-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf379-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf379-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf379-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf379-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf379-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf379-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bf379-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bf379-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf379-124">**TB \_ MAPACCELERATORW** (Unicode) y **TB \_ MAPACCELERATORA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf379-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





