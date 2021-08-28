---
description: El método SetValue agrega un nuevo valor PROPVARIANT o sobrescribe uno existente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: Método IPortableDeviceValues::SetValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f6af975b2876a177207df4f57bfe1f76d78a4b7239ce6d9c4cfcab52f0cf9042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055045"
---
# <a name="iportabledevicevaluessetvalue-method"></a>IPortableDeviceValues::SetValue (Método)

El **método SetValue** agrega un nuevo **valor PROPVARIANT** o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que** especifica el elemento que se creará o sobrescribirá.

</dd> <dt>

*pValue* \[ En\]
</dt> <dd>

**PROPVARIANT que** especifica el nuevo valor. El SDK copia el valor para que el autor de la llamada pueda liberar la variable local llamando a **PropVariantClear** después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando VARTYPE para *pValue* es VT VECTOR o VT UI1, no se admite el establecimiento de un búfer null o \_ \_ de tamaño  cero. Por ejemplo, no se permiten pValue.caub.pElems = **NULL** ni pValue.caub.cElems = 0.

Este método se puede usar para recuperar un valor de cualquier tipo de la colección. Sin embargo, si conoce el tipo de valor de antemano, use uno de los métodos **Set...** especializados de esta interfaz para evitar la sobrecarga de trabajar directamente con valores PROPVARIANT.

Si un valor existente tiene la misma clave especificada por el parámetro *key,* sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




