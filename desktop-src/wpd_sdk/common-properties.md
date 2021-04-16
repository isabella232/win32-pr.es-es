---
description: Los dispositivos portátiles de Windows (WPD) admiten las siguientes propiedades de los parámetros de comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parámetros de comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718877"
---
# <a name="command-parameters"></a>Parámetros de comando

Los dispositivos portátiles de Windows (WPD) admiten las siguientes propiedades de los parámetros de comando.




| **Propiedad**                                            | **VarType**     | **Descripción**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_información de \_ \_ cliente común \_ de la propiedad WPD**          | **VT \_ desconocido** | Interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que el controlador usa para identificar al cliente.                                                             |
| **\_contexto de \_ \_ información de cliente común \_ \_ de la propiedad WPD** | **VT \_ LPWStr**  | Contexto especificado por el controlador que identifica a un cliente para todas las operaciones posteriores.                                                                                          |
| **propiedad de la \_ \_ categoría de comandos comunes de propiedades de \_ WPD \_**            | **VT \_ CLSID**   | Parte del **GUID** del valor de **PROPERTYKEY** del comando.                                                                                                            |
| **\_identificador de \_ \_ comando común \_ de la propiedad WPD**                  | **VT \_ UI4**     | La parte del identificador único persistente (PID) del valor de **PROPERTYKEY** del comando.                                                                                          |
| **\_destino del \_ \_ comando común \_ de la propiedad WPD**              | **VT \_ LPWStr**  | Identificador del objeto de destino.                                                                                                                                                |
| **\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**          | **VT \_ UI4**     | Código de error específico del controlador devuelto por un controlador de WPD.                                                                                                                       |
| **\_HRESULT de propiedad \_ común \_ de WPD**                      | **ERROR de VT \_**   | Valor **HRESULT** devuelto por un controlador de WPD para una operación determinada.                                                                                                   |
| **\_ \_ \_ identificadores de objeto \_ comunes de la propiedad WPD**                  | **VT \_ desconocido** | Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo Variant **VT \_ LPWStr** que contiene una lista de identificadores de objeto. |
| **\_ \_ \_ \_ identificadores únicos persistentes \_ comunes de la propiedad WPD**      | **VT \_ desconocido** | Una interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo Variant **VT \_ LPWStr** que contiene una lista de PID.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




