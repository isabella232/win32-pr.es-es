---
title: Mensaje de DRV_OPEN (mmsystem. h)
description: Indica al controlador que abra una nueva instancia de.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- Mensaje de DRV_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151133"
---
# <a name="drv_open-message"></a><span data-ttu-id="f2ad9-104">DRV \_ Open Message</span><span class="sxs-lookup"><span data-stu-id="f2ad9-104">DRV\_OPEN message</span></span>

<span data-ttu-id="f2ad9-105">Indica al controlador que abra una nueva instancia de.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2ad9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2ad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ad9-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="f2ad9-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="f2ad9-108">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="f2ad9-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="f2ad9-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="f2ad9-110">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="f2ad9-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f2ad9-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f2ad9-112">Dirección de una cadena de caracteres anchos terminada en null que especifica la información de configuración utilizada para abrir la instancia.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="f2ad9-113">Si no hay información de configuración disponible, significa que esta cadena está vacía o el parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f2ad9-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f2ad9-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f2ad9-115">datos específicos del controlador de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ad9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2ad9-116">Return Value</span></span>

<span data-ttu-id="f2ad9-117">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ad9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2ad9-118">Remarks</span></span>

<span data-ttu-id="f2ad9-119">Si el controlador devuelve un valor distinto de cero, el sistema utiliza ese valor como identificador de controlador (el parámetro *dwDriverId* ) en los mensajes que envía posteriormente a la instancia del controlador.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="f2ad9-120">El controlador puede devolver cualquier tipo de valor como identificador.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="f2ad9-121">Por ejemplo, algunos controladores devuelven direcciones de memoria que apuntan a información específica de la instancia.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="f2ad9-122">El uso de este método para especificar los identificadores de una instancia de controlador proporciona a los controladores acceso a la información mientras están procesando mensajes.</span><span class="sxs-lookup"><span data-stu-id="f2ad9-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ad9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2ad9-123">Requirements</span></span>



| <span data-ttu-id="f2ad9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ad9-124">Requirement</span></span> | <span data-ttu-id="f2ad9-125">Value</span><span class="sxs-lookup"><span data-stu-id="f2ad9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ad9-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2ad9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ad9-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2ad9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2ad9-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2ad9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ad9-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2ad9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f2ad9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2ad9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ad9-131"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2ad9-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ad9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2ad9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ad9-133">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="f2ad9-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="f2ad9-134">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="f2ad9-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





