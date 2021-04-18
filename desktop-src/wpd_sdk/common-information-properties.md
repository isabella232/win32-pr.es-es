---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de información común.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propiedades de información común (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718893"
---
# <a name="common-information-properties"></a>Propiedades de información común

Los dispositivos portátiles de Windows admiten las siguientes propiedades de información común.



| Propiedad                                      | VarType        | Descripción                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **\_notas de \_ información \_ común de WPD**           | **VT \_ LPWStr** | En el caso de citas, tareas y objetos similares, esta propiedad contiene las notas del objeto especificado.     |
| **\_asunto de \_ información \_ común de WPD**         | **VT \_ LPWStr** | Valor que especifica el campo de asunto de este objeto.                                                 |
| **\_ \_ \_ texto del cuerpo de información común de WPD \_**      | **VT \_ LPWStr** | Esta propiedad contiene el texto del cuerpo de un objeto, en formato de texto no cifrado o HTML.                          |
| **\_prioridad de \_ información \_ común de WPD**        | **VT \_ UI4**    | Valor que especifica la prioridad de este objeto. 0 indica la prioridad más alta.                    |
| **\_ \_ \_ fecha y hora de inicio de información común de WPD \_** | **fecha de VT \_**   | Valor que especifica la fecha y hora en que está programada la inicio de una cita, tarea u objeto similar. |
| **\_ \_ \_ fecha y hora de finalización de información común de WPD \_**   | **fecha de VT \_**   | Valor que especifica la fecha y hora en que está programada la finalización de una cita, tarea u objeto similar.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




