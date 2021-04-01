---
title: Mensaje de CBEM_SETIMAGELIST (commctrl. h)
description: Establece una lista de imágenes para un control ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997033"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="08092-104">CBEM \_ SETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="08092-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="08092-105">Establece una lista de imágenes para un control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="08092-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="08092-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08092-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08092-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="08092-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="08092-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="08092-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08092-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08092-110">Identificador de la lista de imágenes que se va a establecer para el control.</span><span class="sxs-lookup"><span data-stu-id="08092-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08092-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08092-111">Return value</span></span>

<span data-ttu-id="08092-112">Devuelve el identificador de la lista de imágenes asociada previamente al control o devuelve **null** si no se ha establecido previamente ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="08092-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="08092-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08092-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08092-114">El alto de las imágenes de la lista de imágenes podría cambiar los requisitos de tamaño del control ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="08092-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="08092-115">Se recomienda que cambie el tamaño del control después de enviar este mensaje para asegurarse de que se muestre correctamente.</span><span class="sxs-lookup"><span data-stu-id="08092-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08092-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08092-116">Requirements</span></span>



| <span data-ttu-id="08092-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08092-117">Requirement</span></span> | <span data-ttu-id="08092-118">Value</span><span class="sxs-lookup"><span data-stu-id="08092-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08092-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08092-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08092-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08092-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08092-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08092-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08092-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="08092-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08092-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08092-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08092-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08092-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





