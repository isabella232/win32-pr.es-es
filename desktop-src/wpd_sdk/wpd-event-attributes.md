---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los eventos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Atributos de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698524"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="e2a39-104">Atributos de evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="e2a39-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="e2a39-105">En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los eventos de un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2a39-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="e2a39-106">Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .</span><span class="sxs-lookup"><span data-stu-id="e2a39-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="e2a39-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="e2a39-107">Attribute</span></span>                             | <span data-ttu-id="e2a39-108">VarType</span><span class="sxs-lookup"><span data-stu-id="e2a39-108">VarType</span></span>         | <span data-ttu-id="e2a39-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2a39-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a39-110">**\_nombre del \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e2a39-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="e2a39-111">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="e2a39-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="e2a39-112">Cadena que especifica el nombre descriptivo del script del evento.</span><span class="sxs-lookup"><span data-stu-id="e2a39-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="e2a39-113">Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="e2a39-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="e2a39-114">**\_Opciones del \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e2a39-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="e2a39-115">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="e2a39-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="e2a39-116">[**IPortableDeviceValues**](iportabledevicevalues.md) que contiene las opciones de evento.</span><span class="sxs-lookup"><span data-stu-id="e2a39-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="e2a39-117">**\_parámetros del \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e2a39-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="e2a39-118">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="e2a39-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="e2a39-119">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="e2a39-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="e2a39-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a39-120">Requirements</span></span>



| <span data-ttu-id="e2a39-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a39-121">Requirement</span></span> | <span data-ttu-id="e2a39-122">Value</span><span class="sxs-lookup"><span data-stu-id="e2a39-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a39-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2a39-123">Header</span></span><br/> | <dl> <span data-ttu-id="e2a39-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a39-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a39-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2a39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a39-126">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="e2a39-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




