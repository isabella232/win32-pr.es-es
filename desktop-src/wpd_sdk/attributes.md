---
description: Windows Dispositivos portátiles admite los siguientes atributos de propiedad.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Atributos de propiedad (PortableDevice.h)
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
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843568"
---
# <a name="property-attributes-portabledeviceh"></a>Atributos de propiedad (PortableDevice.h)

Windows Dispositivos portátiles admite los siguientes atributos de propiedad. Estos atributos los devuelven los métodos siguientes:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Atributo                                           | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EL ATRIBUTO \_ DE PROPIEDAD WPD \_ PUEDE \_ \_ ELIMINAR**           | **VT \_ BOOL**    | Valor booleano que especifica si el cliente puede eliminar la propiedad. Para eliminar una propiedad, establezca su valor en VT \_ EMPTY.                                                                                                                                                                                                                                                                   |
| **EL ATRIBUTO \_ DE PROPIEDAD WPD \_ PUEDE \_ \_ LEER**             | **VT \_ BOOL**    | Valor booleano que especifica si el cliente puede leer la propiedad .                                                                                                                                                                                                                                                                                                                       |
| **EL ATRIBUTO \_ DE PROPIEDAD \_ WPD PUEDE \_ \_ ESCRIBIR**            | **VT \_ BOOL**    | Valor booleano que especifica si el cliente puede modificar la propiedad.                                                                                                                                                                                                                                                                                                                     |
| **VALOR PREDETERMINADO \_ DEL ATRIBUTO DE PROPIEDAD \_ \_ \_ WPD**        | VT \_ *XXXX*      | Valor definido por el dispositivo que especifica el valor predeterminado de una propiedad. Esto solo se aplica a las propiedades que se pueden escribir.                                                                                                                                                                                                                                                               |
| **ELEMENTOS DE \_ ENUMERACIÓN DE \_ ATRIBUTOS DE \_ PROPIEDAD \_ WPD** | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene una colección de valores para una propiedad cuyo atributo **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM** es **WPD PROPERTY ATTRIBUTE \_ FORM \_ \_ \_ ENUMERATION**. El tipo de datos depende de la propiedad que se está consultando.                                                                              |
| **WPD \_ PROPERTY ATTRIBUTE FAST \_ \_ \_ PROPERTY**        | **VT \_ BOOL**    | Si es True, esta propiedad pertenece al grupo *de propiedades rápidas.* Estas son propiedades que se pueden recuperar del dispositivo rápidamente.                                                                                                                                                                                                                                                        |
| **FORMULARIO DE ATRIBUTO \_ DE \_ PROPIEDAD \_ WPD**                  | **VT \_ UI4**     | Valor [**enumerado WpdAttributeForm**](wpdattributeform.md) que especifica la forma de los valores válidos permitidos para esta propiedad.                                                                                                                                                                                                                                                         |
| **NOMBRE DEL ATRIBUTO \_ DE \_ PROPIEDAD \_ WPD**                  | **VT \_ LPWSTR**  | Cadena que especifica el nombre descriptivo del script de la propiedad. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y ' \_ '.                                                                                                                                                                                                                                                                    |
| **INTERVALO MÁXIMO DE \_ ATRIBUTOS \_ DE PROPIEDAD \_ WPD \_**            | VT \_ *XXXX*      | Valor máximo de una propiedad cuyo atributo **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM** es **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE**. El tipo de datos puede ser cualquiera de los tipos numéricos.                                                                                                                                                                                                               |
| **INTERVALO MÍNIMO DE \_ ATRIBUTOS \_ DE PROPIEDAD \_ WPD \_**            | VT \_ *XXXX*      | Valor mínimo de una propiedad cuyo atributo **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM** es **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE**. El tipo de datos puede ser cualquiera de los tipos numéricos.                                                                                                                                                                                                               |
| **PASO DE INTERVALO DE \_ \_ ATRIBUTOS DE PROPIEDAD \_ WPD \_**           | VT \_ *XXXX*      | Valor del paso para una propiedad cuyo atributo **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM** es **WPD PROPERTY ATTRIBUTE FORM \_ \_ \_ \_ RANGE**. El paso especifica cuánto debe cambiar una propiedad de intervalo. Por ejemplo, una propiedad con un valor mínimo de 10, un valor máximo de 20 y un paso de 5 podría tener los siguientes valores: **10**, **15**, **20**. El tipo de datos puede ser cualquiera de los tipos numéricos. |
| **EXPRESIÓN REGULAR \_ DEL ATRIBUTO DE PROPIEDAD \_ \_ \_ WPD**   | **VT \_ LPWSTR**  | Cadena de expresión regular que especifica valores aceptables para las propiedades cuyo formulario es **WPD \_ PROPERTY ATTRIBUTE FORM REGULAR \_ \_ \_ \_ EXPRESSION**.                                                                                                                                                                                                                                             |
| **ATRIBUTO DE \_ PROPIEDAD \_ \_ WPD VARTYPE**               | **VT \_ UI4**     | Entero que especifica el VARTYPE de la propiedad, por ejemplo, **VT \_ BOOL.**                                                                                                                                                                                                                                                                                                              |
| **TAMAÑO MÁXIMO DEL \_ ATRIBUTO \_ DE PROPIEDAD \_ WPD \_**             | **VT \_ UI8**     | Valor que especifica el tamaño máximo para el valor de esta propiedad, en bytes.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades**](properties-and-attributes.md)
</dt> </dl>

 

 




