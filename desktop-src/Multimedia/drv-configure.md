---
title: Mensaje de DRV_CONFIGURE (mmsystem. h)
description: Dirige el controlador instalable para mostrar su cuadro de diálogo de configuración y permitir que el usuario especifique la nueva configuración para la instancia de controlador instalable especificada.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Mensaje de DRV_CONFIGURE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997093"
---
# <a name="drv_configure-message"></a><span data-ttu-id="04037-104">DRV \_ configurar mensaje</span><span class="sxs-lookup"><span data-stu-id="04037-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="04037-105">Dirige el controlador instalable para mostrar su cuadro de diálogo de configuración y permitir que el usuario especifique la nueva configuración para la instancia de controlador instalable especificada.</span><span class="sxs-lookup"><span data-stu-id="04037-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="04037-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04037-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="04037-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="04037-108">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="04037-108">Identifier of the installable driver.</span></span> <span data-ttu-id="04037-109">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="04037-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="04037-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="04037-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="04037-111">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="04037-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="04037-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="04037-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="04037-113">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="04037-113">Handle of the parent window.</span></span> <span data-ttu-id="04037-114">Esta ventana se utiliza como ventana primaria para el cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="04037-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="04037-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="04037-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="04037-116">Dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="04037-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="04037-117">Si se proporciona la estructura, contiene los nombres de la clave del registro y el valor asociado al controlador.</span><span class="sxs-lookup"><span data-stu-id="04037-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04037-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04037-118">Return Value</span></span>

<span data-ttu-id="04037-119">Devuelve uno de estos valores:</span><span class="sxs-lookup"><span data-stu-id="04037-119">Returns one of these values:</span></span>



| <span data-ttu-id="04037-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04037-120">Requirement</span></span> | <span data-ttu-id="04037-121">Value</span><span class="sxs-lookup"><span data-stu-id="04037-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04037-122">DRVCNF \_ Aceptar</span><span class="sxs-lookup"><span data-stu-id="04037-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="04037-123">La configuración es correcta; no es necesario realizar ninguna otra acción.</span><span class="sxs-lookup"><span data-stu-id="04037-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="04037-124">\_Cancelar DRVCNF</span><span class="sxs-lookup"><span data-stu-id="04037-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="04037-125">El usuario canceló el cuadro de diálogo. no es necesario realizar ninguna otra acción.</span><span class="sxs-lookup"><span data-stu-id="04037-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="04037-126">reinicio de DRVCNF \_</span><span class="sxs-lookup"><span data-stu-id="04037-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="04037-127">La configuración es correcta, pero los cambios no surten efecto hasta que se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="04037-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="04037-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04037-128">Remarks</span></span>

<span data-ttu-id="04037-129">Algunos controladores instalables anexan información de configuración al valor asignado al valor del registro asociado al controlador.</span><span class="sxs-lookup"><span data-stu-id="04037-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="04037-130">Los \_ valores de devolución DRV CANCEL, DRV \_ OK y DRV \_ restart son obsoletos; se han sustituido por DRVCNF \_ Cancel, DRVCNF \_ OK y DRVCNF \_ restart, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="04037-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="04037-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04037-131">Requirements</span></span>



| <span data-ttu-id="04037-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="04037-132">Requirement</span></span> | <span data-ttu-id="04037-133">Value</span><span class="sxs-lookup"><span data-stu-id="04037-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04037-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04037-134">Minimum supported client</span></span><br/> | <span data-ttu-id="04037-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04037-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04037-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04037-136">Minimum supported server</span></span><br/> | <span data-ttu-id="04037-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04037-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="04037-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04037-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="04037-139"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04037-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04037-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="04037-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04037-141">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="04037-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="04037-142">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="04037-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

