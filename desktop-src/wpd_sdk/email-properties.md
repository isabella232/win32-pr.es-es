---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de correo electrónico.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propiedades de correo electrónico (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680387"
---
# <a name="email-properties"></a>Propiedades de correo electrónico

Los dispositivos portátiles de Windows admiten las siguientes propiedades de correo electrónico.



| Propiedad                         | VarType        | Descripción                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **\_línea CCO de correo electrónico de WPD \_ \_**        | **VT \_ LPWStr** | Destinatarios de CCO del mensaje de correo electrónico. Los destinatarios CCO reciben una copia del mensaje de correo electrónico, pero sus nombres no se muestran como destinatarios.   |
| **\_línea CC de correo electrónico de WPD \_ \_**         | **VT \_ LPWStr** | Destinatarios de CC del mensaje de correo electrónico. Los destinatarios de CC reciben una copia del mensaje de correo electrónico y sus nombres se muestran como destinatarios. |
| **el \_ correo electrónico de WPD \_ tiene \_ datos adjuntos** | **VT \_ bool**   | Valor booleano que especifica si este mensaje de correo electrónico tiene datos adjuntos.                                                               |
| **se \_ ha \_ \_ leído el correo electrónico de WPD \_**  | **VT \_ bool**   | Valor booleano que especifica si se ha leído este mensaje de correo electrónico.                                                                 |
| **\_hora de recepción de correo electrónico de WPD \_ \_**   | **fecha de VT \_**   | Valor que especifica cuándo se recibió el mensaje de correo electrónico.                                                                              |
| **\_dirección del remitente de correo electrónico de WPD \_ \_**  | **VT \_ LPWStr** | La dirección de correo electrónico del remitente.                                                                                                         |
| **\_correo electrónico \_ de WPD en \_ línea**         | **VT \_ LPWStr** | Los destinatarios principales del mensaje de correo electrónico.                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




