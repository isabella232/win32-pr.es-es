---
title: Mensaje de TB_SETDISABLEDIMAGELIST (commctrl. h)
description: Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar botones deshabilitados.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079605"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="edeb3-104">\_Mensaje SETDISABLEDIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="edeb3-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="edeb3-105">Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar botones deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="edeb3-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="edeb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edeb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edeb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edeb3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edeb3-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edeb3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="edeb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edeb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edeb3-110">Identificador de la lista de imágenes que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="edeb3-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edeb3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edeb3-111">Return value</span></span>

<span data-ttu-id="edeb3-112">Devuelve el identificador de la lista de imágenes que se usó anteriormente para mostrar botones deshabilitados, o **null** si no se ha establecido previamente ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="edeb3-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="edeb3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edeb3-113">Requirements</span></span>



| <span data-ttu-id="edeb3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="edeb3-114">Requirement</span></span> | <span data-ttu-id="edeb3-115">Value</span><span class="sxs-lookup"><span data-stu-id="edeb3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edeb3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edeb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="edeb3-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edeb3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edeb3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edeb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="edeb3-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="edeb3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edeb3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edeb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="edeb3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edeb3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





