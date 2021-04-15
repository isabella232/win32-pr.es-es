---
title: Mensaje de RB_PUSHCHEVRON (commctrl. h)
description: Se envía a un control rebar para presionar mediante programación un botón de contenido adicional.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534660"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="afaff-104">Mensaje de PUSHCHEVRON de RB \_</span><span class="sxs-lookup"><span data-stu-id="afaff-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="afaff-105">Se envía a un control rebar para presionar mediante programación un botón de contenido adicional.</span><span class="sxs-lookup"><span data-stu-id="afaff-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="afaff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afaff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afaff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afaff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afaff-108">Índice de base cero de la banda cuyo cheurón se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="afaff-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="afaff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afaff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afaff-110">Un valor de 32 bits definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="afaff-110">An application defined 32-bit value.</span></span> <span data-ttu-id="afaff-111">Se devolverá a la aplicación como el miembro **lParamNM** de la estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que se pasa con la notificación [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="afaff-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afaff-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afaff-112">Return value</span></span>

<span data-ttu-id="afaff-113">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="afaff-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="afaff-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afaff-114">Remarks</span></span>

<span data-ttu-id="afaff-115">Cuando se envía este mensaje, el control rebar enviará a la aplicación un código de notificación [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , que le pedirá que muestre el menú de comillas angulares.</span><span class="sxs-lookup"><span data-stu-id="afaff-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="afaff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afaff-116">Requirements</span></span>



| <span data-ttu-id="afaff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="afaff-117">Requirement</span></span> | <span data-ttu-id="afaff-118">Value</span><span class="sxs-lookup"><span data-stu-id="afaff-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afaff-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="afaff-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="afaff-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afaff-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="afaff-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="afaff-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afaff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afaff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="afaff-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afaff-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





