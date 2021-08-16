---
description: Windows Dispositivos portátiles admite las siguientes propiedades de extensión de clase.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Propiedades de extensión de clase (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c7215a383aec582f576cb64a6781068034bb7fa8df03b5a404368482f1c1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843409"
---
# <a name="class-extension-properties"></a>Propiedades de extensión de clase

Windows Dispositivos portátiles admite las siguientes propiedades de extensión de clase.



| Propiedad                                                                      | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TIPOS DE CONTENIDO ADMITIDOS EN LAS OPCIONES \_ DE EXTENSIÓN DE CLASE \_ \_ \_ \_ WPD \_**                 | **VT \_ UNKNOWN** | Valor que especifica la lista (superconjunto) de tipos de contenido admitidos por el controlador (similar a llamar a FUNCIONES DE COMANDO WPD OBTENER TIPOS DE CONTENIDO ADMITIDOs en \_ \_ \_ \_ \_ \_ **WPD \_ FUNCTIONAL CATEGORY \_ \_ ALL**).                                                                                                                                                                                                                                                                                                                                             |
| **LAS OPCIONES DE \_ EXTENSIÓN \_ DE CLASE \_ WPD NO REGISTRAN LA \_ INTERFAZ DE DISPOSITIVO \_ \_ \_ \_ WPD**    | **VT \_ BOOL**    | Valor que especifica si el autor de la llamada desea que la biblioteca de extensiones de clase WPD registre la interfaz clase de dispositivo WPD. Si este valor es true, el autor de la llamada asume la responsabilidad del registro.<br/> Si este valor es false, indica que el autor de la llamada espera que la biblioteca de extensiones de clase realice el registro.<br/>La mayoría de los controladores deben permitir que la biblioteca de extensiones de clase realice el registro, excepto en los casos en los que el registro de la interfaz de clase de dispositivo WPD por parte de la biblioteca de extensiones de clase pueda producir efectos negativos. |
| **OPCIONES DE \_ EXTENSIÓN DE \_ CLASE WPD REGISTRAR INTERFAZ \_ DE DISPOSITIVO PRIVADO \_ \_ \_ \_ \_ WPD** | **VT \_ BOOL**    | Indica que el autor de la llamada quiere que la biblioteca de extensiones de clase WPD registre la interfaz de clase de dispositivo WPD privada. Esto no se recomienda para la mayoría de los controladores. Solo se debe usar en casos en los que el registro de la interfaz de clase de dispositivo WPD por parte de la biblioteca de extensiones de clase cause efectos negativos. Esta opción se usa normalmente junto con **WPD \_ CLASS EXTENSION OPTIONS \_ \_ \_ DONT REGISTER \_ \_ WPD DEVICE \_ \_ INTERFACE** establecido en **TRUE.**                                                                                          |
| **VALORES DE IDENTIFICACIÓN \_ DEL DISPOSITIVO DE OPCIONES DE EXTENSIÓN DE \_ \_ \_ \_ CLASE \_ WPD**            | **VT \_ UNKNOWN** | Se trata de [un valor IPortableDeviceValues](iportabledevicevalues.md) que contiene los valores de identificación del dispositivo **(WPD \_ DEVICE \_ MANUFACTURER**, **WPD DEVICE \_ \_ MODEL**, **WPD \_ DEVICE FIRMWARE \_ \_ VERSION** e **WPD DEVICE FUNCTIONAL \_ UNIQUE \_ \_ \_ ID**). Incluir esto con otras opciones de extensión de clase al inicializar                                                                                                                                                                                                                               |
| **ANCHO DE BANDA DE \_ TRANSPORTE DE OPCIONES DE EXTENSIÓN DE \_ \_ \_ CLASE WPD \_**                      | **VT \_ UI4**     | Indica el ancho de banda máximo teórico del transporte en kilobits por segundo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **VALORES DE IDENTIFICACIÓN \_ DEL DISPOSITIVO DE OPCIONES DE EXTENSIÓN DE \_ \_ \_ \_ CLASE \_ WPD**            | **VT \_ UNKNOWN** | Se trata de [un valor IPortableDeviceValues](iportabledevicevalues.md) que contiene los valores de identificación del dispositivo **(WPD \_ DEVICE \_ MANUFACTURER**, **WPD DEVICE \_ \_ MODEL**, **WPD \_ DEVICE FIRMWARE \_ \_ VERSION** e **WPD DEVICE FUNCTIONAL \_ UNIQUE \_ \_ \_ ID**). Incluya esto con otras opciones de extensión de clase al inicializar.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




