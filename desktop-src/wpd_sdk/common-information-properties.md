---
description: Windows Dispositivos portátiles admite las siguientes propiedades de información comunes.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propiedades de información comunes (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571225"
---
# <a name="common-information-properties"></a>Propiedades de información comunes

Windows Dispositivos portátiles admite las siguientes propiedades de información comunes.



| Propiedad                                      | VarType        | Descripción                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **NOTAS DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD**           | **VT \_ LPWSTR** | Para citas, tareas y objetos similares, esta propiedad contiene las notas del objeto especificado.     |
| **ASUNTO DE \_ INFORMACIÓN COMÚN \_ DE \_ WPD**         | **VT \_ LPWSTR** | Valor que especifica el campo asunto de este objeto.                                                 |
| **TEXTO DEL CUERPO \_ DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD**      | **VT \_ LPWSTR** | Esta propiedad contiene el texto del cuerpo de un objeto, en formato html o texto sin formato.                          |
| **PRIORIDAD DE INFORMACIÓN \_ \_ COMÚN DE \_ WPD**        | **VT \_ UI4**    | Valor que especifica la prioridad de este objeto. 0 indica la prioridad más alta.                    |
| **WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME** | **VT \_ DATE**   | Valor que especifica la fecha y hora en que se programa el inicio de una cita, una tarea u otro objeto similar. |
| **WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME**   | **VT \_ DATE**   | Valor que especifica la fecha y hora en que está programada la finalización de una cita, una tarea u otro objeto similar.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




