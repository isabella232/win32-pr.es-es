---
title: Mensaje EM_GETOPTIONS (RichEdit. h)
description: Recupera opciones enriquecidas de control de edición.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996745"
---
# <a name="em_getoptions-message"></a><span data-ttu-id="7c79e-104">\_Mensaje GETOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="7c79e-104">EM\_GETOPTIONS message</span></span>

<span data-ttu-id="7c79e-105">Recupera opciones enriquecidas de control de edición.</span><span class="sxs-lookup"><span data-stu-id="7c79e-105">Retrieves rich edit control options.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c79e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c79e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c79e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c79e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c79e-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7c79e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c79e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c79e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c79e-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7c79e-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c79e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c79e-111">Return value</span></span>

<span data-ttu-id="7c79e-112">Este mensaje devuelve una combinación de los valores de marca de la opción actual descritos en el mensaje [**\_ SETOPTIONS em**](em-setoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="7c79e-112">This message returns a combination of the current option flag values described in the [**EM\_SETOPTIONS**](em-setoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c79e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c79e-113">Requirements</span></span>



| <span data-ttu-id="7c79e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c79e-114">Requirement</span></span> | <span data-ttu-id="7c79e-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c79e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c79e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c79e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c79e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7c79e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c79e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c79e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c79e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c79e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c79e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c79e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c79e-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c79e-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c79e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c79e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c79e-123">**\_SETOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="7c79e-123">**EM\_SETOPTIONS**</span></span>](em-setoptions.md)
</dt> </dl>

 

 





