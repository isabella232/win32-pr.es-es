---
description: Las \_ constantes de marcador de bits LINEGATHERTERM describen las condiciones en las que se termina la recopilación de dígitos almacenados en búfer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes de LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681215"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="5bc95-103">Constantes de LINEGATHERTERM \_</span><span class="sxs-lookup"><span data-stu-id="5bc95-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="5bc95-104">Las constantes de marcador de bits **LINEGATHERTERM \_** describen las condiciones en las que se termina la recopilación de dígitos almacenados en búfer.</span><span class="sxs-lookup"><span data-stu-id="5bc95-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="5bc95-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**</span><span class="sxs-lookup"><span data-stu-id="5bc95-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5bc95-106">Se ha recopilado el número solicitado de dígitos.</span><span class="sxs-lookup"><span data-stu-id="5bc95-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="5bc95-107">El búfer está lleno.</span><span class="sxs-lookup"><span data-stu-id="5bc95-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5bc95-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**\_Cancelar LINEGATHERTERM**</span><span class="sxs-lookup"><span data-stu-id="5bc95-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5bc95-109">La solicitud fue cancelada por esta aplicación, por otra aplicación o porque la llamada finalizó.</span><span class="sxs-lookup"><span data-stu-id="5bc95-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5bc95-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="5bc95-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5bc95-111">El primer dígito agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="5bc95-111">The first digit timeout expired.</span></span> <span data-ttu-id="5bc95-112">El búfer no contiene dígitos.</span><span class="sxs-lookup"><span data-stu-id="5bc95-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5bc95-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM de \_ tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="5bc95-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5bc95-114">Expiró el tiempo de espera entre dígitos.</span><span class="sxs-lookup"><span data-stu-id="5bc95-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="5bc95-115">El búfer contiene al menos un dígito.</span><span class="sxs-lookup"><span data-stu-id="5bc95-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5bc95-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**</span><span class="sxs-lookup"><span data-stu-id="5bc95-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5bc95-117">Uno de los dígitos de finalización coincidió con un dígito recibido.</span><span class="sxs-lookup"><span data-stu-id="5bc95-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="5bc95-118">El dígito de finalización coincidente es el último dígito del búfer.</span><span class="sxs-lookup"><span data-stu-id="5bc95-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc95-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bc95-119">Remarks</span></span>

<span data-ttu-id="5bc95-120">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="5bc95-120">No extensibility.</span></span> <span data-ttu-id="5bc95-121">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="5bc95-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc95-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc95-122">Requirements</span></span>



| <span data-ttu-id="5bc95-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc95-123">Requirement</span></span> | <span data-ttu-id="5bc95-124">Value</span><span class="sxs-lookup"><span data-stu-id="5bc95-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5bc95-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5bc95-125">TAPI version</span></span><br/> | <span data-ttu-id="5bc95-126">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5bc95-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5bc95-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bc95-127">Header</span></span><br/>       | <dl> <span data-ttu-id="5bc95-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc95-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




