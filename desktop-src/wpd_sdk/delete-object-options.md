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
# <a name="delete_object_options-enumeration"></a>ELIMINAR \_ la \_ enumeración de opciones de objeto

El tipo de enumeración **Delete \_ Object \_ Options** describe las opciones admitidas por un dispositivo al eliminar un objeto.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_eliminación de dispositivo portátil \_ \_ sin \_ recursividad**
</dt> <dd>

Elimine solo el objeto y genere un error si tiene elementos secundarios.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ eliminación de dispositivos portátiles \_ con \_ recursividad**
</dt> <dd>

Elimine el objeto y todos sus elementos secundarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación puede recuperar las opciones de eliminación que admite el dispositivo mediante una llamada a [**IPortableDeviceCapabilities:: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para el comando de **eliminación de \_ \_ \_ \_ \_ objetos de administración de objetos de comandos de WPD** . Debe examinar el valor de la opción [](iportabledevicevaluescollection.md) compatible con el método de **\_ \_ \_ \_ \_ \_ eliminación recursiva de administración de objetos** de la opción de WPD que este método devuelve en un objeto IPortableDeviceValuesCollection.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




