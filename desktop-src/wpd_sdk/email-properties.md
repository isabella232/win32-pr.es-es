---
description: Windows Dispositivos portátiles admite las siguientes propiedades de correo electrónico.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propiedades de correo electrónico (PortableDevice.h)
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
ms.openlocfilehash: 4c67a341bcc7fcac041f02cc183c02e024e60b121150aba0ce62da2f973ccbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843237"
---
# <a name="email-properties"></a>Propiedades de correo electrónico

Windows Dispositivos portátiles admite las siguientes propiedades de correo electrónico.



| Propiedad                         | VarType        | Descripción                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ EMAIL \_ BCC \_ LINE**        | **VT \_ LPWSTR** | Destinatarios BCC del mensaje de correo electrónico. Los destinatarios de BCC reciben una copia del correo electrónico, pero sus nombres no se muestran como destinatarios.   |
| **WPD \_ EMAIL \_ CC \_ LINE**         | **VT \_ LPWSTR** | Destinatarios cc del mensaje de correo electrónico. Los destinatarios cc reciben una copia del mensaje de correo electrónico y sus nombres se muestran como destinatarios. |
| **EL CORREO ELECTRÓNICO DE WPD \_ \_ TIENE DATOS \_ ADJUNTOS** | **VT \_ BOOL**   | Valor booleano que especifica si este mensaje de correo electrónico tiene datos adjuntos.                                                               |
| **SE HA \_ LEÍDO EL CORREO ELECTRÓNICO DE \_ \_ \_ WPD**  | **VT \_ BOOL**   | Valor booleano que especifica si se ha leído este mensaje de correo electrónico.                                                                 |
| **HORA DE RECIBIR \_ CORREO \_ ELECTRÓNICO DE \_ WPD**   | **FECHA \_ DE VT**   | Valor que especifica cuándo se recibió el mensaje de correo electrónico.                                                                              |
| **DIRECCIÓN DEL REMITENTE \_ DE CORREO ELECTRÓNICO DE \_ \_ WPD**  | **VT \_ LPWSTR** | La dirección de correo electrónico del remitente.                                                                                                         |
| **CORREO ELECTRÓNICO DE WPD \_ \_ A \_ LÍNEA**         | **VT \_ LPWSTR** | Los destinatarios principales del mensaje de correo electrónico.                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




