---
description: El mensaje SENDMSPDATA de la línea de TSPI \_ se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Mensaje de LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690225"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="2b8d3-103">Mensaje de línea \_ SENDMSPDATA</span><span class="sxs-lookup"><span data-stu-id="2b8d3-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="2b8d3-104">El mensaje **\_ SENDMSPDATA** de la línea de TSPI se envía cuando el proveedor de servicios de telefonía (TSP) desea pasar información al proveedor de servicios multimedia (MSP).</span><span class="sxs-lookup"><span data-stu-id="2b8d3-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2b8d3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b8d3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b8d3-106">*htLine*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-107">Identificador de TAPI de la línea.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-108">*htCall*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-109">Identificador de TAPI de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-110">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-111">La línea de valor \_ SENDMSPDATA.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-113">Identifica el MSP que debe recibir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="2b8d3-114">Si es 0, el mensaje se enviará a todos los MSP.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="2b8d3-115">Este es el identificador que se pasa a la [**función \_ LineCreateMSPInstance de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .</span><span class="sxs-lookup"><span data-stu-id="2b8d3-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-117">Búfer que se va a pasar al MSP.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="2b8d3-118">TAPI no interpreta el búfer.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="2b8d3-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8d3-120">Tamaño, en bytes, del búfer en *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b8d3-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8d3-121">Remarks</span></span>

<span data-ttu-id="2b8d3-122">El proveedor de servicios debe negociar una versión de TAPI 3,0 o posterior para que este mensaje funcione.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8d3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8d3-123">Requirements</span></span>



| <span data-ttu-id="2b8d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8d3-124">Requirement</span></span> | <span data-ttu-id="2b8d3-125">Value</span><span class="sxs-lookup"><span data-stu-id="2b8d3-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2b8d3-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2b8d3-126">TAPI version</span></span><br/> | <span data-ttu-id="2b8d3-127">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="2b8d3-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="2b8d3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b8d3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2b8d3-129"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d3-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8d3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8d3-131">Acerca del proveedor de servicios multimedia (MSP)</span><span class="sxs-lookup"><span data-stu-id="2b8d3-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="2b8d3-132">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="2b8d3-133">**TSPI \_ LineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="2b8d3-134">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="2b8d3-135">**TSPI \_ lineRecieveMSPData**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="2b8d3-136">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

