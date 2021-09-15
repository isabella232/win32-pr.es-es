---
description: El tipo de enumeración DELETE OBJECT OPTIONS describe las opciones que admite un \_ dispositivo al eliminar un \_ objeto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS enumeración (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466467"
---
# <a name="delete_object_options-enumeration"></a>DELETE \_ OBJECT \_ OPTIONS (enumeración)

El **tipo \_ de \_ enumeración DELETE OBJECT OPTIONS** describe las opciones que admite un dispositivo al eliminar un objeto.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**ELIMINACIÓN \_ DE DISPOSITIVO PORTÁTIL SIN \_ \_ \_ RECURSIVIDAD**
</dt> <dd>

Elimine solo el objeto y se producirá un error si tiene elementos secundarios.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**ELIMINACIÓN \_ DE \_ DISPOSITIVOS \_ \_ PORTÁTILES CON RECURSIVIDAD**
</dt> <dd>

Elimine el objeto y todos sus elementos secundarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación puede recuperar las opciones de eliminación que admite el dispositivo llamando a [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para el comando **WPD \_ COMMAND OBJECT MANAGEMENT DELETE \_ \_ \_ \_ OBJECTS.** Debe examinar el valor de la opción **WPD \_ OPTION OBJECT MANAGEMENT \_ \_ \_ RECURSIVE \_ DELETE \_ SUPPORTED** que este método devuelve en un [**objeto IPortableDeviceValuesCollection.**](iportabledevicevaluescollection.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




