---
description: El método GetIPortableDeviceValuesCollectionValue recupera un valor de IPortableDeviceValuesCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708705"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (método)

El método **GetIPortableDeviceValuesCollectionValue** recupera un valor de **IPORTABLEDEVICEVALUESCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*ppValue* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperada. El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es una interfaz **IPortableDeviceValuesCollection** .<br/> |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/>                                |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, consulte [recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[Recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




