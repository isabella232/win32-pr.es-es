---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades varias.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propiedades varias (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670649"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="27232-103">Propiedades varias</span><span class="sxs-lookup"><span data-stu-id="27232-103">Miscellaneous Properties</span></span>

<span data-ttu-id="27232-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades varias.</span><span class="sxs-lookup"><span data-stu-id="27232-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="27232-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27232-105">Property</span></span>                                       | <span data-ttu-id="27232-106">VarType</span><span class="sxs-lookup"><span data-stu-id="27232-106">VarType</span></span>         | <span data-ttu-id="27232-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="27232-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27232-108">**la opción de la API de WPD \_ \_ \_ usar \_ Clear \_ Data \_ Stream**</span><span class="sxs-lookup"><span data-stu-id="27232-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="27232-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="27232-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="27232-110">Un valor booleano que especifica si el flujo de datos creado para la transferencia de datos será claro, es decir, DRM no está implicado. Los clientes pueden establecer esta opción agregándolas a las propiedades de objeto que se pasan a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="27232-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="27232-111">**\_versión del servicio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="27232-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="27232-112">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="27232-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="27232-113">Cadena que especifica la versión de implementación de un servicio de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="27232-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="27232-114">**tipos de contenido de la carpeta de WPD \_ \_ \_ \_ permitidos**</span><span class="sxs-lookup"><span data-stu-id="27232-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="27232-115">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="27232-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="27232-116">Valor que especifica los tipos de objeto que pueden ser elementos secundarios directos de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="27232-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="27232-117">Las carpetas secundarias pueden tener diferentes capacidades. Esta propiedad es una [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene \_ los valores CLSID de VT que especifican los tipos de objeto permitidos.</span><span class="sxs-lookup"><span data-stu-id="27232-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="27232-118">Para obtener una lista de tipos de objetos definidos por dispositivos portátiles de Windows, consulte [requisitos de objetos](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="27232-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="27232-119">**\_categoría de \_ objeto \_ funcional de WPD**</span><span class="sxs-lookup"><span data-stu-id="27232-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="27232-120">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="27232-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="27232-121">Valor que especifica la categoría funcional del objeto.</span><span class="sxs-lookup"><span data-stu-id="27232-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="27232-122">**perfiles de información de representación de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27232-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="27232-123">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="27232-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="27232-124">[**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) que contiene varias interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , cada una de las cuales contiene los valores de propiedad de un perfil que admite el objeto.</span><span class="sxs-lookup"><span data-stu-id="27232-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="27232-125">**nombre para mostrar de la ubicación de la \_ sugerencia de objeto WPD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27232-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="27232-126">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="27232-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="27232-127">Si un objeto es una ubicación de sugerencia, esta propiedad indica el nombre específico de la sugerencia que se va a mostrar al usuario en lugar del nombre del objeto. Los controladores pueden especificar sugerencias de ubicación para varios tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="27232-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="27232-128">Se trata de ubicaciones de almacenamiento preferidas para las carpetas que contienen un tipo de objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="27232-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="27232-129">Un equivalente sería la carpeta Mis imágenes para los archivos de imagen de Windows.</span><span class="sxs-lookup"><span data-stu-id="27232-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="27232-130">Si esta propiedad no existe, normalmente se usa [el \_ \_ nombre del objeto WPD](object-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="27232-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27232-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27232-131">Requirements</span></span>



| <span data-ttu-id="27232-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="27232-132">Requirement</span></span> | <span data-ttu-id="27232-133">Value</span><span class="sxs-lookup"><span data-stu-id="27232-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="27232-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27232-134">Header</span></span><br/> | <dl> <span data-ttu-id="27232-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="27232-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27232-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="27232-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27232-137">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="27232-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




