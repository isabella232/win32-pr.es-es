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
ms.openlocfilehash: e5c58652c27d62e2954e86b9170e2f0a2d4ae4021743ced769adbf46a1f082b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431062"
---
# <a name="command-parameters"></a>Parámetros de comando

Windows Dispositivos portátiles (WPD) admite las siguientes propiedades de parámetros de comando.




| **Propiedad**                                            | **VarType**     | **Descripción**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INFORMACIÓN DE CLIENTE \_ COMÚN DE \_ LA \_ PROPIEDAD \_ WPD**          | **VT \_ UNKNOWN** | Interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que el controlador usa para identificar al cliente.                                                             |
| **CONTEXTO DE INFORMACIÓN DE CLIENTE \_ COMÚN DE LA PROPIEDAD \_ \_ \_ \_ WPD** | **VT \_ LPWSTR**  | Contexto especificado por el controlador que identifica un cliente para todas las operaciones posteriores.                                                                                          |
| **WPD \_ PROPERTY \_ COMMON \_ COMMAND \_ CATEGORY**            | **VT \_ CLSID**   | Parte **GUID** del valor **PROPERTYKEY** del comando.                                                                                                            |
| **WPD \_ PROPERTY \_ COMMON \_ COMMAND \_ ID**                  | **VT \_ UI4**     | Parte del identificador único persistente (PID) del **valor PROPERTYKEY** del comando.                                                                                          |
| **DESTINO DE COMANDO \_ COMÚN DE LA \_ PROPIEDAD WPD \_ \_**              | **VT \_ LPWSTR**  | Identificador de objeto de destino.                                                                                                                                                |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD**          | **VT \_ UI4**     | Código de error específico del controlador devuelto por un controlador WPD.                                                                                                                       |
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**                      | **\_ERROR DE VT**   | Valor **HRESULT** devuelto por un controlador WPD para una operación determinada.                                                                                                   |
| **IDENTIFICADORES DE OBJETOS \_ \_ COMUNES DE LA \_ \_ PROPIEDAD WPD**                  | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo **variante VT \_ LPWSTR que** contiene una lista de identificadores de objeto. |
| **IDENTIFICADORES \_ \_ ÚNICOS PERSISTENTES \_ COMUNES DE LA \_ \_ PROPIEDAD WPD**      | **VT \_ UNKNOWN** | Interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo **variante VT \_ LPWSTR que** contiene una lista de PID.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




