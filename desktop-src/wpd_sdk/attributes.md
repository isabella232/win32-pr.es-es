---
description: Los dispositivos portátiles de Windows admiten los siguientes atributos de propiedad.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Atributos de propiedad (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 9e48a4f81a6223ed034f6de14fe104a1a2aa4393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700082"
---
# <a name="property-attributes-portabledeviceh"></a>Atributos de propiedad (PortableDevice. h)

Los dispositivos portátiles de Windows admiten los siguientes atributos de propiedad. Estos atributos se devuelven mediante los métodos siguientes:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Atributo                                           | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **el \_ atributo de propiedad de WPD \_ \_ puede \_ eliminar**           | **VT \_ bool**    | Valor booleano que especifica si el cliente puede eliminar la propiedad. Para eliminar una propiedad, establezca su valor en VT \_ vacío.                                                                                                                                                                                                                                                                   |
| **el \_ atributo de propiedad de WPD \_ \_ puede \_ leer**             | **VT \_ bool**    | Valor booleano que especifica si el cliente puede leer la propiedad.                                                                                                                                                                                                                                                                                                                       |
| **el \_ atributo de propiedad de WPD \_ \_ puede \_ escribir**            | **VT \_ bool**    | Valor booleano que especifica si el cliente puede modificar la propiedad.                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ valor predeterminado del atributo de propiedad de \_ WPD \_**        | VT \_ *xxxx*      | Un valor definido por el dispositivo que especifica el valor predeterminado de una propiedad. Esto solo se aplica a las propiedades que se escriben.                                                                                                                                                                                                                                                               |
| **\_elementos de \_ \_ enumeración de atributos de propiedad de WPD \_** | **VT \_ desconocido** | Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene una colección de valores para una propiedad cuyo atributo de formulario de **atributo de propiedad de WPD \_ \_ \_** es la **\_ \_ \_ \_ enumeración de formulario de atributo de propiedad WPD**. El tipo de datos depende de la propiedad que se consulta.                                                                              |
| **\_ \_ propiedad rápida del atributo de propiedad de \_ WPD \_**        | **VT \_ bool**    | Si es true, esta propiedad pertenece al grupo *propiedades rápidas* . Se trata de propiedades que se pueden recuperar rápidamente del dispositivo.                                                                                                                                                                                                                                                        |
| **\_formulario de \_ atributo de propiedad de WPD \_**                  | **VT \_ UI4**     | Valor enumerado de [**WpdAttributeForm**](wpdattributeform.md) que especifica la forma de los valores válidos permitidos para esta propiedad.                                                                                                                                                                                                                                                         |
| **\_nombre del \_ atributo de propiedad de WPD \_**                  | **VT \_ LPWStr**  | Cadena que especifica el nombre descriptivo del script de la propiedad. Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.                                                                                                                                                                                                                                                                    |
| **\_ \_ \_ intervalo máximo de atributos de propiedad de WPD \_**            | VT \_ *xxxx*      | El valor máximo de una propiedad cuyo atributo de formulario de atributo de propiedad de WPD es el **intervalo del formulario de atributo de propiedad de WPD \_ \_ \_ \_**. **\_ \_ \_** El tipo de datos puede ser cualquiera de los tipos numéricos.                                                                                                                                                                                                               |
| **\_ \_ \_ intervalo mínimo de atributos de propiedad de WPD \_**            | VT \_ *xxxx*      | El valor mínimo de una propiedad cuyo atributo de formulario de atributo de propiedad de WPD es el **intervalo del formulario de atributo de propiedad de WPD \_ \_ \_ \_**. **\_ \_ \_** El tipo de datos puede ser cualquiera de los tipos numéricos.                                                                                                                                                                                                               |
| **\_paso de \_ intervalo de atributos de propiedad de WPD \_ \_**           | VT \_ *xxxx*      | El valor de paso de una propiedad cuyo atributo de formulario de atributo de propiedad de WPD es el **intervalo de formulario de \_ atributo de propiedad \_ \_ \_ WPD**. **\_ \_ \_** El paso especifica la cantidad que debe cambiar una propiedad de intervalo. Por ejemplo, una propiedad con un valor mínimo de 10, un valor máximo de 20 y un paso de 5 pueden tener los siguientes valores: **10**, **15**, **20**. El tipo de datos puede ser cualquiera de los tipos numéricos. |
| **\_ \_ expresión regular del atributo de propiedad de \_ WPD \_**   | **VT \_ LPWStr**  | Una cadena de expresión regular que especifica valores aceptables para las propiedades cuyo formulario es una **\_ \_ \_ \_ \_ expresión regular del formulario de atributo de propiedad de WPD**.                                                                                                                                                                                                                                             |
| **atributo de propiedad de WPD \_ \_ \_ VARTYPE**               | **VT \_ UI4**     | Un entero que especifica el VARTYPE de la propiedad, por ejemplo, **VT \_ bool**.                                                                                                                                                                                                                                                                                                              |
| **\_ \_ tamaño máximo del atributo de propiedad de \_ WPD \_**             | **VT \_ UI8**     | Valor que especifica el tamaño máximo para el valor de esta propiedad, en bytes.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades**](properties-and-attributes.md)
</dt> </dl>

 

 




