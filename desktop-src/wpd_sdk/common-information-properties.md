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
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431108"
---
# <a name="common-information-properties"></a>Propiedades de información comunes

Windows Dispositivos portátiles admite las siguientes propiedades de información comunes.



| Propiedad                                      | VarType        | Descripción                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **NOTAS DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD**           | **VT \_ LPWSTR** | Para citas, tareas y objetos similares, esta propiedad contiene las notas del objeto especificado.     |
| **ASUNTO DE \_ INFORMACIÓN COMÚN \_ DE \_ WPD**         | **VT \_ LPWSTR** | Valor que especifica el campo asunto de este objeto.                                                 |
| **TEXTO DEL CUERPO \_ DE \_ INFORMACIÓN \_ COMÚN DE \_ WPD**      | **VT \_ LPWSTR** | Esta propiedad contiene el texto del cuerpo de un objeto, en formato html o texto no cifrado.                          |
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

 

 




