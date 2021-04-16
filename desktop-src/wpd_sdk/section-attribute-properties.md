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
# <a name="section-attribute-properties"></a>Propiedades de los atributos de sección

Los dispositivos portátiles de Windows admiten las siguientes propiedades de datos de sección.



| Propiedad                                             | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **longitud de los datos de la \_ sección WPD \_ \_**                       | **VT \_ UI8**     | Especifica la longitud del objeto al que se hace referencia.                                                                                                                                                                                                                                                                                              |
| **\_desplazamiento de \_ datos de sección de WPD \_**                       | **VT \_ UI8**     | Especifica el desplazamiento de base cero de los datos para el objeto al que se hace referencia.                                                                                                                                                                                                                                                                      |
| **\_recursos de \_ objeto de referencia de datos de sección de \_ \_ WPD \_** | **VT \_ desconocido** | Un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene un valor único que especifica la clave de un recurso determinado. Este recurso es el objeto al que hace referencia el desplazamiento de datos de la sección de WPD \_ \_ y la longitud de \_ datos de la \_ sección WPD \_ \_ .<br/> Si esta propiedad no existe, \_ \_ se supone el valor predeterminado del recurso WPD.<br/> |
| **unidades de datos de la \_ sección WPD \_ \_**                        | **VT \_ UI4**     | Especifica las unidades utilizadas para este desplazamiento, por ejemplo, bytes, milisegundos, etc. Los valores posibles para esta propiedad se definen en la sección de los valores de unidades de datos de la **\_ sección \_ \_ \_ WPD** en el archivo PortableDevice. h.<br/> Si no se especifica ninguna unidad, se supone que se trata de bytes.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




