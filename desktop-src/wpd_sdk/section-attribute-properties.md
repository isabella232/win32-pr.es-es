---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de datos de sección.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propiedades de los atributos de sección (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718967"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="53dad-103">Propiedades de los atributos de sección</span><span class="sxs-lookup"><span data-stu-id="53dad-103">Section Attribute Properties</span></span>

<span data-ttu-id="53dad-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de datos de sección.</span><span class="sxs-lookup"><span data-stu-id="53dad-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="53dad-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53dad-105">Property</span></span>                                             | <span data-ttu-id="53dad-106">VarType</span><span class="sxs-lookup"><span data-stu-id="53dad-106">VarType</span></span>         | <span data-ttu-id="53dad-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="53dad-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53dad-108">**longitud de los datos de la \_ sección WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53dad-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="53dad-109">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="53dad-109">**VT\_UI8**</span></span>     | <span data-ttu-id="53dad-110">Especifica la longitud del objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="53dad-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="53dad-111">**\_desplazamiento de \_ datos de sección de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53dad-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="53dad-112">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="53dad-112">**VT\_UI8**</span></span>     | <span data-ttu-id="53dad-113">Especifica el desplazamiento de base cero de los datos para el objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="53dad-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="53dad-114">**\_recursos de \_ objeto de referencia de datos de sección de \_ \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53dad-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="53dad-115">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="53dad-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="53dad-116">Un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene un valor único que especifica la clave de un recurso determinado. Este recurso es el objeto al que hace referencia el desplazamiento de datos de la sección de WPD \_ \_ y la longitud de \_ datos de la \_ sección WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="53dad-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="53dad-117">Si esta propiedad no existe, \_ \_ se supone el valor predeterminado del recurso WPD.</span><span class="sxs-lookup"><span data-stu-id="53dad-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="53dad-118">**unidades de datos de la \_ sección WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="53dad-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="53dad-119">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="53dad-119">**VT\_UI4**</span></span>     | <span data-ttu-id="53dad-120">Especifica las unidades utilizadas para este desplazamiento, por ejemplo, bytes, milisegundos, etc. Los valores posibles para esta propiedad se definen en la sección de los valores de unidades de datos de la **\_ sección \_ \_ \_ WPD** en el archivo PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="53dad-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="53dad-121">Si no se especifica ninguna unidad, se supone que se trata de bytes.</span><span class="sxs-lookup"><span data-stu-id="53dad-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="53dad-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53dad-122">Requirements</span></span>



| <span data-ttu-id="53dad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="53dad-123">Requirement</span></span> | <span data-ttu-id="53dad-124">Value</span><span class="sxs-lookup"><span data-stu-id="53dad-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53dad-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53dad-125">Header</span></span><br/> | <dl> <span data-ttu-id="53dad-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="53dad-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53dad-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="53dad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53dad-128">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="53dad-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




