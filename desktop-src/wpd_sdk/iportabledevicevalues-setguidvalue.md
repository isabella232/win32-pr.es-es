---
description: El método SetGuidValue agrega un nuevo valor GUID (Type VT \_ CLSID) o sobrescribe uno existente.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'IPortableDeviceValues:: SetGuidValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708892"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a>IPortableDeviceValues:: SetGuidValue (método)

El método **SetGuidValue** agrega un nuevo valor **GUID** (Type VT \_ CLSID) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

**REFGUID** que contiene el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Agregar un recurso a un objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




