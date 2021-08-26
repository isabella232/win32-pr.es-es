---
description: Para Windows 7, Windows Portable Devices admite los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Atributos de parámetro (PortableDevice.h)
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
ms.openlocfilehash: 8004f4e2f9f7c22d795b6ce4e4cb0affac1b55ecd876c21288c02e226ee14262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006115"
---
# <a name="parameter-attributes"></a>Atributos de parámetro

Para Windows 7, Windows Portable Devices admite los siguientes atributos de parámetro para los métodos y eventos de un servicio de dispositivo. Estos métodos devuelven estos atributos:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Atributo                                            | VarType         | Descripción                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VALOR PREDETERMINADO \_ DEL ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD**        | VT \_ *XXXX*      | Valor predeterminado del parámetro.                                                                                                                                                         |
| **ELEMENTOS DE \_ ENUMERACIÓN DE \_ ATRIBUTOS DE \_ PARÁMETRO WPD \_** | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene los valores de enumeración del parámetro .                                   |
| **FORMULARIO DE ATRIBUTO \_ DE PARÁMETRO \_ WPD \_**                  | **VT \_ UI4**     | Forma de valores de parámetro válidos permitidos.                                                                                                                                                 |
| **TAMAÑO MÁXIMO DEL \_ ATRIBUTO \_ DE PARÁMETRO \_ WPD \_**             | **VT \_ UI8**     | Tamaño máximo del parámetro, en bytes .                                                                                                                                               |
| **NOMBRE DEL ATRIBUTO \_ DE PARÁMETRO \_ WPD \_**                  | **VT \_ LPWSTR**  | Cadena que especifica el nombre descriptivo del script de un evento o parámetro de método. Los caracteres válidos son alfanuméricos \[ a-zA-Z0-9 \] y ' \_ '.                                                 |
| **WPD \_ PARAMETER \_ ATTRIBUTE \_ ORDER**                 | **VT \_ UI4**     | Índice de orden de parámetros de base cero, de modo que un valor de pedido de 0 se corresponda con el primer parámetro.                                                                                       |
| **INTERVALO MÍNIMO DE \_ ATRIBUTOS \_ DE PARÁMETRO \_ WPD \_**            | VT \_ *XXXX*      | Valor máximo de un parámetro con el formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **WPD \_ PARAMETER \_ ATTRIBUTE \_ RANGE \_ MAX**            | VT \_ *XXXX*      | Valor mínimo para un parámetro con el formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **PASO DE INTERVALO \_ DE ATRIBUTOS DE PARÁMETRO \_ \_ WPD \_**           | VT \_ *XXXX*      | Valor del paso para un parámetro con el formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                          |
| **EXPRESIÓN REGULAR \_ DEL ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD**   | **VT \_ LPWSTR**  | Expresión regular que especifica valores aceptables para parámetros con el formato WPD \_ PARAMETER ATTRIBUTE FORM REGULAR \_ \_ \_ \_ EXPRESSION.                                                      |
| **TIPO DE USO \_ DEL ATRIBUTO DE PARÁMETRO \_ \_ WPD \_**           | **VT \_ UI4**     | Entero que especifica el uso de un parámetro de método, por ejemplo, in/out. Los valores válidos son del tipo [**de \_ enumeración WPD PARAMETER \_ USAGE \_ TYPES.**](wpd-parameter-usage-types.md) |
| **ATRIBUTO DE \_ PARÁMETRO \_ \_ WPD VARTYPE**               | **VT \_ UI4**     | Parámetro VarType.                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




