---
description: Las \_ constantes de marcador de bits LINETRANSFERMODE describen diferentes maneras de resolver las solicitudes de transferencia de llamadas.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes de LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679061"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="ed11f-103">Constantes de LINETRANSFERMODE \_</span><span class="sxs-lookup"><span data-stu-id="ed11f-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="ed11f-104">Las constantes de marcador de bits **LINETRANSFERMODE \_** describen diferentes maneras de resolver las solicitudes de transferencia de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ed11f-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="ed11f-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**Conferencia de LINETRANSFERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="ed11f-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ed11f-106">La transferencia se resuelve mediante el establecimiento de una conferencia de tres vías entre la aplicación, la entidad conectada a la llamada inicial y la entidad conectada a la llamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="ed11f-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="ed11f-107">Cuando se selecciona esta opción, se crea una llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="ed11f-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed11f-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**transferencia de LINETRANSFERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="ed11f-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ed11f-109">La transferencia se resuelve transfiriendo la llamada inicial a la llamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="ed11f-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="ed11f-110">Ambas llamadas se volverán inactivas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed11f-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed11f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed11f-111">Remarks</span></span>

<span data-ttu-id="ed11f-112">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="ed11f-112">No extensibility.</span></span> <span data-ttu-id="ed11f-113">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ed11f-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed11f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed11f-114">Requirements</span></span>



| <span data-ttu-id="ed11f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed11f-115">Requirement</span></span> | <span data-ttu-id="ed11f-116">Value</span><span class="sxs-lookup"><span data-stu-id="ed11f-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ed11f-117">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ed11f-117">TAPI version</span></span><br/> | <span data-ttu-id="ed11f-118">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ed11f-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ed11f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed11f-119">Header</span></span><br/>       | <dl> <span data-ttu-id="ed11f-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed11f-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




