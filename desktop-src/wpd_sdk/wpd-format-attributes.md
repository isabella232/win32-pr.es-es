---
description: 'En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los formatos de un servicio de dispositivo. Estos atributos son devueltos por el método IPortableDeviceServiceCapabilities:: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Atributos de formato (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671010"
---
# <a name="format-attributes"></a><span data-ttu-id="24323-104">Atributos de formato</span><span class="sxs-lookup"><span data-stu-id="24323-104">Format Attributes</span></span>

<span data-ttu-id="24323-105">En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos para los formatos de un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24323-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="24323-106">Estos atributos son devueltos por el método [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .</span><span class="sxs-lookup"><span data-stu-id="24323-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="24323-107">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="24323-107">**Attribute**</span></span>                        | <span data-ttu-id="24323-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="24323-108">**VarType**</span></span>    | <span data-ttu-id="24323-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24323-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24323-110">**\_atributo de formato WPD \_ \_ Mimetype**</span><span class="sxs-lookup"><span data-stu-id="24323-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="24323-111">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="24323-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24323-112">El tipo MIME de formato.</span><span class="sxs-lookup"><span data-stu-id="24323-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="24323-113">**\_nombre del \_ atributo de formato WPD \_**</span><span class="sxs-lookup"><span data-stu-id="24323-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="24323-114">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="24323-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24323-115">Cadena que especifica el nombre descriptivo del script del formato.</span><span class="sxs-lookup"><span data-stu-id="24323-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="24323-116">Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="24323-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="24323-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24323-117">Requirements</span></span>



| <span data-ttu-id="24323-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24323-118">Requirement</span></span> | <span data-ttu-id="24323-119">Value</span><span class="sxs-lookup"><span data-stu-id="24323-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="24323-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24323-120">Header</span></span><br/> | <dl> <span data-ttu-id="24323-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="24323-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24323-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="24323-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24323-123">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="24323-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




