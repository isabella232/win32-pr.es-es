---
title: Mensaje de CBEM_GETIMAGELIST (commctrl. h)
description: Obtiene el identificador de una lista de imágenes asignada a un control ComboBoxEx.
ms.assetid: d577f920-b8f7-4d51-9507-765b7f925408
keywords:
- CBEM_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d143b8483fb5fb97ebd65fa2a98640089f6d548
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658343"
---
# <a name="cbem_getimagelist-message"></a><span data-ttu-id="f640e-104">CBEM \_ GETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="f640e-104">CBEM\_GETIMAGELIST message</span></span>

<span data-ttu-id="f640e-105">Obtiene el identificador de una lista de imágenes asignada a un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="f640e-105">Gets the handle to an image list assigned to a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f640e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f640e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f640e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f640e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f640e-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f640e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f640e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f640e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f640e-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f640e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f640e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f640e-111">Return value</span></span>

<span data-ttu-id="f640e-112">Devuelve el identificador de la lista de imágenes asignada al control si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f640e-112">Returns the handle to the image list assigned to the control if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f640e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f640e-113">Requirements</span></span>



| <span data-ttu-id="f640e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f640e-114">Requirement</span></span> | <span data-ttu-id="f640e-115">Value</span><span class="sxs-lookup"><span data-stu-id="f640e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f640e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f640e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f640e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f640e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f640e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f640e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f640e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f640e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f640e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f640e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f640e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f640e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





