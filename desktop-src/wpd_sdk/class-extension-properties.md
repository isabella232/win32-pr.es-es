---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de extensión de clase.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Propiedades de la extensión de clase (PortableDevice. h)
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
ms.openlocfilehash: c7e961b80ae990653e6c354640b35c28f8bcf8b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699462"
---
# <a name="class-extension-properties"></a>Propiedades de extensión de clase

Los dispositivos portátiles de Windows admiten las siguientes propiedades de extensión de clase.



| Propiedad                                                                      | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_tipos de \_ \_ \_ contenido admitido de opciones de \_ extensión de clase WPD \_**                 | **VT \_ desconocido** | Valor que especifica la lista (superconjunto) de tipos de contenido admitidos por el controlador (similar a la llamada a funciones de comando de WPD \_ \_ \_ obtener \_ tipos de contenido admitidos \_ \_ en **\_ \_ categoría \_ funcional de WPD**).                                                                                                                                                                                                                                                                                                                                             |
| **las opciones de extensión de clase de WPD no \_ \_ \_ \_ \_ registran la \_ \_ interfaz de dispositivo WPD \_**    | **VT \_ bool**    | Valor que especifica si el llamador desea que la biblioteca de extensiones de clase WPD registre la interfaz de clase de dispositivo WPD. Si este valor es true, el llamador asume la responsabilidad del registro.<br/> Si este valor es false, indica que el llamador espera que la biblioteca de extensiones de clase realice el registro.<br/>La mayoría de los controladores deben permitir que la biblioteca de extensiones de clase realice el registro, excepto en el caso de que el registro de la interfaz de clase de dispositivo WPD por la biblioteca de extensiones de clase pueda producir efectos negativos. |
| **\_las opciones de extensión de clase de WPD \_ \_ \_ registran la \_ \_ \_ interfaz de dispositivo privado de WPD \_** | **VT \_ bool**    | Indica que el llamador desea que la biblioteca de extensiones de clase WPD registre la interfaz de clase de dispositivo WPD privada. Esto no se recomienda para la mayoría de los controladores. Solo se debería utilizar en casos en los que el registro de la interfaz de clase de dispositivo WPD por la biblioteca de extensiones de clase cause efectos negativos. Esta opción se usa normalmente junto con **\_ las opciones de extensión de clase de WPD no \_ registrar la interfaz de \_ \_ \_ \_ \_ dispositivo \_ de WPD** establecida en **true** .                                                                                          |
| **Opciones de extensión de clase de WPD \_ \_ valores de \_ \_ identificación de dispositivos \_ \_**            | **VT \_ desconocido** | Se trata de un [IPortableDeviceValues](iportabledevicevalues.md) que contiene los valores de identificación del dispositivo (**\_ \_ fabricante del dispositivo de WPD**, **\_ \_ modelo de dispositivo** de WPD, **\_ \_ \_ versión de firmware del dispositivo** de WPD y **\_ \_ \_ \_ identificador único funcional del dispositivo WPD**). Incluir esto en otras opciones de extensión de clase al inicializar                                                                                                                                                                                                                               |
| **\_Opciones de extensión de clase WPD ancho de \_ \_ \_ banda de transporte \_**                      | **VT \_ UI4**     | Indica el ancho de banda máximo teórico del transporte en kilobits por segundo                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Opciones de extensión de clase de WPD \_ \_ valores de \_ \_ identificación de dispositivos \_ \_**            | **VT \_ desconocido** | Se trata de un [IPortableDeviceValues](iportabledevicevalues.md) que contiene los valores de identificación del dispositivo (**\_ \_ fabricante del dispositivo de WPD**, **\_ \_ modelo de dispositivo** de WPD, **\_ \_ \_ versión de firmware del dispositivo** de WPD y **\_ \_ \_ \_ identificador único funcional del dispositivo WPD**). Inclúyalo con otras opciones de extensión de clase al inicializar.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




