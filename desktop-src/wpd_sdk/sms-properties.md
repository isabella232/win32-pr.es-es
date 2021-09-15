---
description: Windows Dispositivos portátiles admite las siguientes propiedades de SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propiedades de SMS (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572040"
---
# <a name="sms-properties"></a>Propiedades de SMS

Windows Dispositivos portátiles admite las siguientes propiedades de SMS.



| Propiedad                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CODIFICACIÓN \_ DE SMS \_ WPD**     | **VT \_ LPWSTR** | Valor que especifica cómo codificará el controlador el mensaje de texto enviado por el cliente. Se trata de una propiedad de solo lectura; El cliente no puede especificar qué tipo de codificación usa un dispositivo para enviar mensajes. Estos valores duplican los valores [**enumerados de WPD \_ SMS ENCODING \_ \_ TYPES.**](wpd-sms-encoding-types.md) |
| **CARGA MÁXIMA DE \_ SMS \_ \_ WPD** | **VT \_ UI4**    | Número máximo de bytes que se pueden contener en un mensaje.                                                                                                                                                                                                                                             |
| **PROVEEDOR DE \_ SMS \_ WPD**     | **VT \_ LPWSTR** | Nombre del proveedor de servicios.                                                                                                                                                                                                                                                                                |
| **TIEMPO DE ESPERA \_ DE SMS \_ DE WPD**      | **VT \_ UI4**    | Número de milisegundos hasta que se devuelve un tiempo de espera.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




