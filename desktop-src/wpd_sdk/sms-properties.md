---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propiedades de SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718711"
---
# <a name="sms-properties"></a>Propiedades de SMS

Los dispositivos portátiles de Windows admiten las siguientes propiedades de SMS.



| Propiedad                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_codificación de SMS de WPD \_**     | **VT \_ LPWStr** | Valor que especifica cómo el controlador codificará el mensaje de texto enviado por el cliente. Se trata de una propiedad de solo lectura; el cliente no puede especificar el tipo de codificación que usa un dispositivo para enviar mensajes. Estos valores duplican los valores enumerados de los [**tipos de codificación de SMS de WPD \_ \_ \_**](wpd-sms-encoding-types.md) . |
| **\_ \_ carga máxima de SMS de WPD \_** | **VT \_ UI4**    | Número máximo de bytes que pueden incluirse en un mensaje.                                                                                                                                                                                                                                             |
| **\_proveedor de SMS de WPD \_**     | **VT \_ LPWStr** | Nombre del proveedor de servicios.                                                                                                                                                                                                                                                                                |
| **tiempo de espera de \_ SMS de WPD \_**      | **VT \_ UI4**    | El número de milisegundos hasta que se devuelve un tiempo de espera.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




