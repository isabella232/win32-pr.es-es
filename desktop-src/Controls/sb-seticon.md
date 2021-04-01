---
title: Mensaje de SB_SETICON (commctrl. h)
description: Establece el icono de un elemento en una barra de estado.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905456"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="31c0b-104">\_Mensaje SETICON de SB</span><span class="sxs-lookup"><span data-stu-id="31c0b-104">SB\_SETICON message</span></span>

<span data-ttu-id="31c0b-105">Establece el icono de un elemento en una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="31c0b-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="31c0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31c0b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31c0b-108">Índice de base cero del elemento que recibirá el icono.</span><span class="sxs-lookup"><span data-stu-id="31c0b-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="31c0b-109">Si este parámetro es-1, se supone que la barra de estado es una barra de estado simple.</span><span class="sxs-lookup"><span data-stu-id="31c0b-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="31c0b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31c0b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31c0b-111">Identificador del icono que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="31c0b-111">Handle to the icon to be set.</span></span> <span data-ttu-id="31c0b-112">Si este valor es **null**, el icono se quita del elemento.</span><span class="sxs-lookup"><span data-stu-id="31c0b-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c0b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31c0b-113">Return value</span></span>

<span data-ttu-id="31c0b-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="31c0b-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c0b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31c0b-115">Remarks</span></span>

<span data-ttu-id="31c0b-116">La barra de estado no destruirá el icono.</span><span class="sxs-lookup"><span data-stu-id="31c0b-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="31c0b-117">Es responsabilidad de la aplicación que realiza la llamada realizar un seguimiento de los iconos y destruirlos.</span><span class="sxs-lookup"><span data-stu-id="31c0b-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c0b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31c0b-118">Requirements</span></span>



| <span data-ttu-id="31c0b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c0b-119">Requirement</span></span> | <span data-ttu-id="31c0b-120">Value</span><span class="sxs-lookup"><span data-stu-id="31c0b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31c0b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31c0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31c0b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31c0b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31c0b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31c0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31c0b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="31c0b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31c0b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31c0b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c0b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31c0b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





