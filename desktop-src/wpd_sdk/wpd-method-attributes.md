---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los métodos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Atributos de método (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699552"
---
# <a name="method-attributes"></a><span data-ttu-id="3afb3-104">Atributos de método</span><span class="sxs-lookup"><span data-stu-id="3afb3-104">Method Attributes</span></span>

<span data-ttu-id="3afb3-105">En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los métodos de un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3afb3-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="3afb3-106">Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .</span><span class="sxs-lookup"><span data-stu-id="3afb3-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="3afb3-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="3afb3-107">Attribute</span></span>                                      | <span data-ttu-id="3afb3-108">VarType</span><span class="sxs-lookup"><span data-stu-id="3afb3-108">VarType</span></span>         | <span data-ttu-id="3afb3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3afb3-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3afb3-110">**\_ \_ acceso a atributos del método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3afb3-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="3afb3-111">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="3afb3-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="3afb3-112">Acceso al método necesario.</span><span class="sxs-lookup"><span data-stu-id="3afb3-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="3afb3-113">**\_ \_ formato asociado al atributo de método WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3afb3-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="3afb3-114">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="3afb3-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="3afb3-115">Formato asociado al método o **GUID \_ null** si no hay ningún formato asociado.</span><span class="sxs-lookup"><span data-stu-id="3afb3-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="3afb3-116">**\_nombre del \_ atributo del método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3afb3-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="3afb3-117">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="3afb3-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="3afb3-118">Cadena que especifica el nombre descriptivo del script del método.</span><span class="sxs-lookup"><span data-stu-id="3afb3-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="3afb3-119">Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="3afb3-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="3afb3-120">**\_parámetros de \_ atributo del método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3afb3-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="3afb3-121">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="3afb3-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3afb3-122">Una interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene los parámetros del método.</span><span class="sxs-lookup"><span data-stu-id="3afb3-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="3afb3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3afb3-123">Requirements</span></span>



| <span data-ttu-id="3afb3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3afb3-124">Requirement</span></span> | <span data-ttu-id="3afb3-125">Value</span><span class="sxs-lookup"><span data-stu-id="3afb3-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3afb3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3afb3-126">Header</span></span><br/> | <dl> <span data-ttu-id="3afb3-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3afb3-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3afb3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3afb3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3afb3-129">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="3afb3-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




