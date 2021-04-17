---
description: Las \_ constantes de marcador de bits LINEPARKMODE describen diferentes formas de llamadas de estacionamiento.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes de LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690752"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="38edb-103">Constantes de LINEPARKMODE \_</span><span class="sxs-lookup"><span data-stu-id="38edb-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="38edb-104">Las constantes de marcador de bits **LINEPARKMODE \_** describen diferentes formas de llamadas de estacionamiento.</span><span class="sxs-lookup"><span data-stu-id="38edb-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="38edb-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ dirigido**</span><span class="sxs-lookup"><span data-stu-id="38edb-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38edb-106">Especifica el estacionamiento de llamadas dirigido.</span><span class="sxs-lookup"><span data-stu-id="38edb-106">Specifies directed call park.</span></span> <span data-ttu-id="38edb-107">La dirección en la que se va a detener la llamada se debe proporcionar al conmutador.</span><span class="sxs-lookup"><span data-stu-id="38edb-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38edb-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE no \_ Directed**</span><span class="sxs-lookup"><span data-stu-id="38edb-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38edb-109">Especifica el parque de llamadas no directas.</span><span class="sxs-lookup"><span data-stu-id="38edb-109">Specifies nondirected call park.</span></span> <span data-ttu-id="38edb-110">El modificador selecciona la dirección en la que se ha detenido la llamada y la proporciona el modificador a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38edb-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38edb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38edb-111">Remarks</span></span>

<span data-ttu-id="38edb-112">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="38edb-112">No extensibility.</span></span> <span data-ttu-id="38edb-113">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="38edb-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="38edb-114">Las **\_ constantes LINEPARKMODE** se usan cuando se estaciona una llamada.</span><span class="sxs-lookup"><span data-stu-id="38edb-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="38edb-115">Consulte las capacidades del dispositivo de dirección de una línea para averiguar qué modo de estacionamiento está disponible.</span><span class="sxs-lookup"><span data-stu-id="38edb-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="38edb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38edb-116">Requirements</span></span>



| <span data-ttu-id="38edb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38edb-117">Requirement</span></span> | <span data-ttu-id="38edb-118">Value</span><span class="sxs-lookup"><span data-stu-id="38edb-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="38edb-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="38edb-119">TAPI version</span></span><br/> | <span data-ttu-id="38edb-120">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="38edb-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="38edb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38edb-121">Header</span></span><br/>       | <dl> <span data-ttu-id="38edb-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="38edb-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




