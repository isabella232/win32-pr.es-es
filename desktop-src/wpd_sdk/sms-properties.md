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
ms.openlocfilehash: 12b68a962fc79dd75d6ff90635be5dbe99f36c3170f06cd7d79af2eb23317e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193586"
---
# <a name="sms-properties"></a>Propiedades de SMS

Windows Dispositivos portátiles admite las siguientes propiedades de SMS.



| Propiedad                   | VarType        | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CODIFICACIÓN \_ DE SMS \_ WPD**     | **VT \_ LPWSTR** | Valor que especifica cómo codificará el controlador el mensaje de texto enviado por el cliente. Se trata de una propiedad de solo lectura; El cliente no puede especificar qué tipo de codificación usa un dispositivo para enviar mensajes. Estos valores duplican los valores enumerados de [**\_ WPD SMS \_ ENCODING \_ TYPES.**](wpd-sms-encoding-types.md) |
| **CARGA MÁXIMA \_ DE SMS \_ WPD \_** | **VT \_ UI4**    | Número máximo de bytes que se pueden contener en un mensaje.                                                                                                                                                                                                                                             |
| **PROVEEDOR DE \_ SMS \_ WPD**     | **VT \_ LPWSTR** | Nombre del proveedor de servicios.                                                                                                                                                                                                                                                                                |
| **TIEMPO DE ESPERA DE SMS DE WPD \_ \_**      | **VT \_ UI4**    | Número de milisegundos hasta que se devuelve un tiempo de espera.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




