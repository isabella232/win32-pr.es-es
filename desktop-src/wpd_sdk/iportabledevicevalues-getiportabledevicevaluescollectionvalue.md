---
description: El método GetIPortableDeviceValuesCollectionValue recupera un valor IPortableDeviceValuesCollection (tipo VT \_ UNKNOWN) especificado por una clave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: Método IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359550"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue (método)

El **método GetIPortableDeviceValuesCollectionValue** recupera un valor **IPortableDeviceValuesCollection** (tipo VT \_ UNKNOWN) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se recuperará.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperada. El autor de la llamada es responsable de **llamar a Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key no* es una **interfaz IPortableDeviceValuesCollection.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>                                |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Recuperar las funcionalidades de representación compatibles con un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[Recuperar las funcionalidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




