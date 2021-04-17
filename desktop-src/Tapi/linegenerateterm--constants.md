---
description: Las \_ constantes de marcador de bits LINEGENERATETERM describen las condiciones en las que se termina la generación de dígitos o tono.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Constantes de LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691047"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="27d4f-103">Constantes de LINEGENERATETERM \_</span><span class="sxs-lookup"><span data-stu-id="27d4f-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="27d4f-104">Las constantes de marcador de bits **LINEGENERATETERM \_** describen las condiciones en las que se termina la generación de dígitos o tono.</span><span class="sxs-lookup"><span data-stu-id="27d4f-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="27d4f-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**\_Cancelar LINEGENERATETERM**</span><span class="sxs-lookup"><span data-stu-id="27d4f-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="27d4f-106">La solicitud de generación de dígitos o tono fue cancelada por esta aplicación, por otra aplicación o porque la llamada finalizó.</span><span class="sxs-lookup"><span data-stu-id="27d4f-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="27d4f-107">Este valor también se puede devolver cuando no se puede completar la generación de dígitos o de tono debido a un error interno del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="27d4f-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27d4f-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ completado**</span><span class="sxs-lookup"><span data-stu-id="27d4f-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="27d4f-109">Se han generado el número solicitado de dígitos o los tonos solicitados para la duración solicitada.</span><span class="sxs-lookup"><span data-stu-id="27d4f-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27d4f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27d4f-110">Remarks</span></span>

<span data-ttu-id="27d4f-111">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="27d4f-111">No extensibility.</span></span> <span data-ttu-id="27d4f-112">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="27d4f-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d4f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d4f-113">Requirements</span></span>



| <span data-ttu-id="27d4f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d4f-114">Requirement</span></span> | <span data-ttu-id="27d4f-115">Value</span><span class="sxs-lookup"><span data-stu-id="27d4f-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27d4f-116">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="27d4f-116">TAPI version</span></span><br/> | <span data-ttu-id="27d4f-117">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="27d4f-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="27d4f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27d4f-118">Header</span></span><br/>       | <dl> <span data-ttu-id="27d4f-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d4f-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




