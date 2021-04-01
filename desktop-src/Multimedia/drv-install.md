---
title: Mensaje de DRV_INSTALL (mmsystem. h)
description: Notifica al controlador que se está instalando. El controlador debe crear e inicializar las claves y los valores del registro necesarios y comprobar que los controladores y el hardware auxiliares estén instalados y configurados correctamente.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- Mensaje de DRV_INSTALL de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997090"
---
# <a name="drv_install-message"></a><span data-ttu-id="38da7-105">DRV ( \_ mensaje de instalación)</span><span class="sxs-lookup"><span data-stu-id="38da7-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="38da7-106">Notifica al controlador que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="38da7-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="38da7-107">El controlador debe crear e inicializar las claves y los valores del registro necesarios y comprobar que los controladores y el hardware auxiliares estén instalados y configurados correctamente.</span><span class="sxs-lookup"><span data-stu-id="38da7-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="38da7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38da7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38da7-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="38da7-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="38da7-110">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="38da7-110">Identifier of the installable driver.</span></span> <span data-ttu-id="38da7-111">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="38da7-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="38da7-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="38da7-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="38da7-113">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="38da7-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="38da7-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="38da7-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="38da7-115">Dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="38da7-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="38da7-116">Si se especifica una estructura, contiene los nombres de la clave del registro y el valor asociado al controlador.</span><span class="sxs-lookup"><span data-stu-id="38da7-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38da7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38da7-117">Return Value</span></span>

<span data-ttu-id="38da7-118">Devuelve uno de estos valores:</span><span class="sxs-lookup"><span data-stu-id="38da7-118">Returns one of these values:</span></span>



| <span data-ttu-id="38da7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38da7-119">Requirement</span></span> | <span data-ttu-id="38da7-120">Value</span><span class="sxs-lookup"><span data-stu-id="38da7-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="38da7-121">DRVCNF \_ Aceptar</span><span class="sxs-lookup"><span data-stu-id="38da7-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="38da7-122">La instalación se realizó correctamente; no es necesario realizar ninguna otra acción.</span><span class="sxs-lookup"><span data-stu-id="38da7-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="38da7-123">\_Cancelar DRVCNF</span><span class="sxs-lookup"><span data-stu-id="38da7-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="38da7-124">Error en la instalación..</span><span class="sxs-lookup"><span data-stu-id="38da7-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="38da7-125">reinicio de DRVCNF \_</span><span class="sxs-lookup"><span data-stu-id="38da7-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="38da7-126">La instalación se realizó correctamente, pero no surtirá efecto hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="38da7-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38da7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38da7-127">Remarks</span></span>

<span data-ttu-id="38da7-128">No se usa el parámetro *lParam1* .</span><span class="sxs-lookup"><span data-stu-id="38da7-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="38da7-129">Algunos controladores instalables anexan información de configuración al valor asignado al valor del registro asociado al controlador.</span><span class="sxs-lookup"><span data-stu-id="38da7-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="38da7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38da7-130">Requirements</span></span>



| <span data-ttu-id="38da7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="38da7-131">Requirement</span></span> | <span data-ttu-id="38da7-132">Value</span><span class="sxs-lookup"><span data-stu-id="38da7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38da7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38da7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38da7-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="38da7-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38da7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38da7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38da7-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38da7-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38da7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38da7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="38da7-138"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38da7-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38da7-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="38da7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38da7-140">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="38da7-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="38da7-141">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="38da7-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

