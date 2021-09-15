---
description: Windows Dispositivos portátiles (WPD) admite las siguientes propiedades de parámetros de comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parámetros de comando (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572124"
---
# <a name="command-parameters"></a>Parámetros de comando

Windows Dispositivos portátiles (WPD) admite las siguientes propiedades de parámetros de comando.




| **Propiedad**                                            | **VarType**     | **Descripción**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INFORMACIÓN DE CLIENTE \_ COMÚN DE LA PROPIEDAD \_ \_ \_ WPD**          | **VT \_ UNKNOWN** | Interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que el controlador usa para identificar al cliente.                                                             |
| **CONTEXTO DE INFORMACIÓN DE CLIENTE \_ COMÚN DE LA PROPIEDAD \_ \_ \_ \_ WPD** | **VT \_ LPWSTR**  | Contexto especificado por el controlador que identifica un cliente para todas las operaciones posteriores.                                                                                          |
| **WPD \_ PROPERTY \_ COMMON \_ COMMAND \_ CATEGORY**            | **VT \_ CLSID**   | Parte **GUID** del valor **PROPERTYKEY** del comando.                                                                                                            |
| **IDENTIFICADOR DE COMANDO \_ COMÚN DE LA PROPIEDAD \_ \_ \_ WPD**                  | **VT \_ UI4**     | Parte del identificador único persistente (PID) del **valor PROPERTYKEY** del comando.                                                                                          |
| **DESTINO DE COMANDO \_ COMÚN DE LA PROPIEDAD \_ \_ \_ WPD**              | **VT \_ LPWSTR**  | Identificador de objeto de destino.                                                                                                                                                |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA PROPIEDAD \_ \_ \_ \_ WPD**          | **VT \_ UI4**     | Código de error específico del controlador devuelto por un controlador WPD.                                                                                                                       |
| **PROPIEDAD WPD \_ \_ COMMON \_ HRESULT**                      | **\_ERROR DE VT**   | Valor **HRESULT devuelto** por un controlador WPD para una operación determinada.                                                                                                   |
| **IDENTIFICADORES DE OBJETO COMUNES DE \_ \_ LA PROPIEDAD \_ \_ WPD**                  | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection de**](iportabledevicepropvariantcollection.md) tipo **variante VT \_ LPWSTR que** contiene una lista de identificadores de objeto. |
| **IDENTIFICADORES \_ ÚNICOS \_ \_ PERSISTENTES \_ COMUNES DE LA \_ PROPIEDAD WPD**      | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection de**](iportabledevicepropvariantcollection.md) tipo **variante VT \_ LPWSTR que** contiene una lista de PID.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




