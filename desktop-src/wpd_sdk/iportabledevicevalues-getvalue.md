---
description: El método GetValue recupera un valor PROPVARIANT especificado por una clave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: Método IPortableDeviceValues::GetValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cce387bfc08c48547603d8b30a3952952f1e2decf70e06986ea4fb477fe4fdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843038"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>IPortableDeviceValues::GetValue (Método)

El **método GetValue** recupera un **valor PROPVARIANT** especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se recuperará.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Puntero al valor **PROPVARIANT recuperado.** El autor de la llamada debe liberar la memoria llamando **a PropVariantClear** cuando haya terminado con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                     |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando VARTYPE para *pValue* es VT VECTOR o VT UI1, no se admite la recuperación de un búfer null \_ \_ o de tamaño cero.  Por ejemplo, no se permiten pValue.caub.pElems = **NULL** ni pValue.caub.cElems = 0.

Este método se puede usar para recuperar un valor de cualquier tipo de la colección. Sin embargo, si conoce el tipo de valor de antemano, use uno de los métodos de recuperación especializados de esta interfaz para evitar la sobrecarga de trabajar directamente con valores PROPVARIANT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues::SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




