---
description: El método GetUnsignedIntegerValue recupera un valor ULONG (tipo VT \_ UI4) especificado por una clave.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues:: GetUnsignedIntegerValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649607"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>IPortableDeviceValues:: GetUnsignedIntegerValue (método)

El método **GetUnsignedIntegerValue** recupera un valor **ULong** (tipo VT \_ UI4) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*pValue* \[ enuncia\]
</dt> <dd>

Puntero al valor **ULong** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es un tipo **ULong** .<br/>  |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/> |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperando métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> <dt>

[Recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




