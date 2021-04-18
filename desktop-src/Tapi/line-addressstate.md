---
description: El \_ mensaje de línea de ADDRESSSTATE TAPI se envía cuando cambia el estado de una dirección en una línea abierta actualmente por la aplicación. La aplicación puede invocar lineGetAddressStatus para determinar el estado actual de la dirección.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Mensaje de LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679367"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="3d25a-104">Mensaje de línea \_ ADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="3d25a-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="3d25a-105">El mensaje de **línea de \_ ADDRESSSTATE** TAPI se envía cuando cambia el estado de una dirección en una línea abierta actualmente por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d25a-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="3d25a-106">La aplicación puede invocar [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) para determinar el estado actual de la dirección.</span><span class="sxs-lookup"><span data-stu-id="3d25a-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3d25a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d25a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d25a-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3d25a-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25a-109">Identificador del dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="3d25a-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="3d25a-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3d25a-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25a-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="3d25a-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="3d25a-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3d25a-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25a-113">Identificador de dirección de la dirección que cambió de estado.</span><span class="sxs-lookup"><span data-stu-id="3d25a-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="3d25a-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3d25a-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25a-115">Estado de la dirección que cambió.</span><span class="sxs-lookup"><span data-stu-id="3d25a-115">The address state that changed.</span></span> <span data-ttu-id="3d25a-116">Puede ser una o varias de las [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d25a-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d25a-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3d25a-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25a-118">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="3d25a-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d25a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d25a-119">Return value</span></span>

<span data-ttu-id="3d25a-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d25a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d25a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d25a-121">Remarks</span></span>

<span data-ttu-id="3d25a-122">El mensaje **line \_ ADDRESSSTATE** se envía a cualquier aplicación que haya abierto el dispositivo de línea y que haya habilitado este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d25a-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="3d25a-123">El envío de este mensaje para los distintos elementos de estado se puede controlar y consultar mediante [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) y [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="3d25a-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="3d25a-124">De forma predeterminada, los informes de estado de direcciones están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="3d25a-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d25a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d25a-125">Requirements</span></span>



| <span data-ttu-id="3d25a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d25a-126">Requirement</span></span> | <span data-ttu-id="3d25a-127">Value</span><span class="sxs-lookup"><span data-stu-id="3d25a-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3d25a-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3d25a-128">TAPI version</span></span><br/> | <span data-ttu-id="3d25a-129">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3d25a-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3d25a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d25a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="3d25a-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d25a-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d25a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d25a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d25a-133">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="3d25a-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="3d25a-134">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="3d25a-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="3d25a-135">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="3d25a-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="3d25a-136">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="3d25a-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="3d25a-137">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="3d25a-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




