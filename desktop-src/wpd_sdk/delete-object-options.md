---
description: El \_ tipo de \_ enumeración Delete Object Options describe las opciones admitidas por un dispositivo al eliminar un objeto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Enumeración DELETE_OBJECT_OPTIONS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708931"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="37e8c-103">ELIMINAR \_ la \_ enumeración de opciones de objeto</span><span class="sxs-lookup"><span data-stu-id="37e8c-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="37e8c-104">El tipo de enumeración **Delete \_ Object \_ Options** describe las opciones admitidas por un dispositivo al eliminar un objeto.</span><span class="sxs-lookup"><span data-stu-id="37e8c-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37e8c-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="37e8c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="37e8c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="37e8c-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_eliminación de dispositivo portátil \_ \_ sin \_ recursividad**</span><span class="sxs-lookup"><span data-stu-id="37e8c-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="37e8c-108">Elimine solo el objeto y genere un error si tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="37e8c-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="37e8c-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ eliminación de dispositivos portátiles \_ con \_ recursividad**</span><span class="sxs-lookup"><span data-stu-id="37e8c-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="37e8c-110">Elimine el objeto y todos sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="37e8c-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37e8c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37e8c-111">Remarks</span></span>

<span data-ttu-id="37e8c-112">La aplicación puede recuperar las opciones de eliminación que admite el dispositivo mediante una llamada a [**IPortableDeviceCapabilities:: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para el comando de **eliminación de \_ \_ \_ \_ \_ objetos de administración de objetos de comandos de WPD** .</span><span class="sxs-lookup"><span data-stu-id="37e8c-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="37e8c-113">Debe examinar el valor de la opción [](iportabledevicevaluescollection.md) compatible con el método de **\_ \_ \_ \_ \_ \_ eliminación recursiva de administración de objetos** de la opción de WPD que este método devuelve en un objeto IPortableDeviceValuesCollection.</span><span class="sxs-lookup"><span data-stu-id="37e8c-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e8c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37e8c-114">Requirements</span></span>



| <span data-ttu-id="37e8c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="37e8c-115">Requirement</span></span> | <span data-ttu-id="37e8c-116">Value</span><span class="sxs-lookup"><span data-stu-id="37e8c-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e8c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37e8c-117">Header</span></span><br/> | <dl> <span data-ttu-id="37e8c-118"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="37e8c-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37e8c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="37e8c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e8c-120">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="37e8c-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




