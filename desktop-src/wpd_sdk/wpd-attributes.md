---
description: En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Atributos de parámetro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718603"
---
# <a name="parameter-attributes"></a>Atributos de parámetro

En Windows 7, los dispositivos portátiles de Windows admiten los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo. Estos atributos son devueltos por estos métodos:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Atributo                                            | VarType         | Descripción                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ valor predeterminado del atributo de parámetro WPD \_ \_**        | VT \_ *xxxx*      | Valor predeterminado del parámetro.                                                                                                                                                         |
| **\_elementos de \_ \_ enumeración de atributo de parámetro WPD \_** | **VT \_ desconocido** | Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene los valores de enumeración para el parámetro.                                   |
| **\_formulario de \_ atributo de parámetro WPD \_**                  | **VT \_ UI4**     | Forma de valores de parámetro válidos permitidos.                                                                                                                                                 |
| **\_ \_ tamaño máximo del atributo de parámetro WPD \_ \_**             | **VT \_ UI8**     | Tamaño máximo del parámetro, en bytes.                                                                                                                                               |
| **\_nombre del \_ atributo del parámetro WPD \_**                  | **VT \_ LPWStr**  | Cadena que especifica el nombre descriptivo del script de un parámetro de método o evento. Los caracteres válidos son alfanuméricos a \[ -Za-z0-9 \] y ' \_ '.                                                 |
| **\_orden de \_ atributo del parámetro WPD \_**                 | **VT \_ UI4**     | Índice de orden de parámetro basado en cero, de modo que un valor de orden de 0 corresponde al primer parámetro.                                                                                       |
| **\_ \_ \_ intervalo mínimo de atributo de parámetro WPD \_**            | VT \_ *xxxx*      | El valor máximo de un parámetro con el formato del formulario de atributo de parámetro de WPD del formulario \_ \_ \_ \_ .                                                                                                       |
| **rango de atributo de parámetro de WPD \_ \_ \_ \_ máx.**            | VT \_ *xxxx*      | El valor mínimo para un parámetro con el formato del formulario de atributo de parámetro de WPD del formulario \_ \_ \_ \_ .                                                                                                       |
| **\_paso de \_ intervalo de atributo de parámetro WPD \_ \_**           | VT \_ *xxxx*      | El valor de paso para un parámetro con el formato de tipo de atributo del parámetro WPD del formulario \_ \_ \_ \_ .                                                                                                          |
| **\_ \_ expresión regular de atributo de parámetro WPD \_ \_**   | **VT \_ LPWStr**  | Una expresión regular que especifica valores aceptables para los parámetros de la \_ forma \_ expresión regular del formulario de atributo de parámetro WPD \_ \_ \_ .                                                      |
| **\_tipo de \_ uso de atributo de parámetro WPD \_ \_**           | **VT \_ UI4**     | Un entero que especifica el uso de un parámetro de método, por ejemplo, in/out. Los valores válidos son del tipo de enumeración de [**tipos de uso de parámetros de WPD \_ \_ \_**](wpd-parameter-usage-types.md) . |
| **atributo de parámetro de WPD \_ \_ \_ VARTYPE**               | **VT \_ UI4**     | Parámetro VarType.                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




