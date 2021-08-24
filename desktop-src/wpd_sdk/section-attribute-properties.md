---
description: Windows Dispositivos portátiles admite las siguientes propiedades de datos de sección.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propiedades de atributo de sección (PortableDevice.h)
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
ms.openlocfilehash: 21c2386175fe2c3117afd722bd9a6762b605acbc51e299d33934d161974db796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704335"
---
# <a name="section-attribute-properties"></a>Propiedades de atributo de sección

Windows Dispositivos portátiles admite las siguientes propiedades de datos de sección.



| Propiedad                                             | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **LONGITUD DE DATOS \_ DE LA SECCIÓN \_ \_ WPD**                       | **VT \_ UI8**     | Especifica la longitud del objeto al que se hace referencia.                                                                                                                                                                                                                                                                                              |
| **DESPLAZAMIENTO DE DATOS \_ DE LA SECCIÓN \_ \_ WPD**                       | **VT \_ UI8**     | Especifica el desplazamiento de base cero de los datos del objeto al que se hace referencia.                                                                                                                                                                                                                                                                      |
| **RECURSO DE OBJETO \_ AL QUE SE HACE REFERENCIA EN DATOS DE LA SECCIÓN \_ \_ \_ \_ WPD** | **VT \_ UNKNOWN** | [**IPortableDeviceKeyCollection que**](iportabledevicekeycollection.md) contiene un valor único que especifica la clave para un recurso determinado. Este recurso es el objeto al que hace referencia WPD \_ SECTION DATA OFFSET y \_ \_ WPD SECTION DATA \_ \_ \_ LENGTH.<br/> Si esta propiedad no existe, se supone WPD \_ RESOURCE \_ DEFAULT.<br/> |
| **UNIDADES DE \_ DATOS DE LA SECCIÓN \_ WPD \_**                        | **VT \_ UI4**     | Especifica las unidades usadas para este desplazamiento, por ejemplo, bytes, milisegundos, y así sucesivamente. Los valores posibles para esta propiedad se definen en la enumeración **WPD \_ SECTION DATA UNITS \_ \_ \_ VALUES** del archivo PortableDevice.h.<br/> Si no se especifica ninguna unidad, se suponen bytes.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




