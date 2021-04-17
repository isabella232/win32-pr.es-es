---
description: El método SetValue agrega un nuevo valor PROPVARIANT o sobrescribe uno existente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues:: SetValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690256"
---
# <a name="iportabledevicevaluessetvalue-method"></a>IPortableDeviceValues:: SetValue (método)

El método **SetValue** agrega un nuevo valor **PROPVARIANT** o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.

</dd> <dt>

*pValue* \[ de\]
</dt> <dd>

**PROPVARIANT** que especifica el nuevo valor. El SDK copia el valor, de modo que el llamador pueda liberar la variable local llamando a **PropVariantClear** después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando el valor de VARTYPE para *pValue* es VT \_ Vector o VT \_ UI1, no se admite la configuración de un búfer **nulo** o de tamaño cero. Por ejemplo, no se permite ningún pValue. Caub. pElems = **null** ni pvalue. Caub. cElems = 0.

Este método se puede utilizar para recuperar un valor de cualquier tipo de la colección. Sin embargo, si conoce el tipo de valor de antemano, use uno de los métodos de **set especializados...** de esta interfaz para evitar la sobrecarga de trabajar directamente con los valores de PROPVARIANT.

Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera adecuadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




