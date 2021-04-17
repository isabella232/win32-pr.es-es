---
description: El método SetBufferValue agrega un nuevo valor de BYTE \* (Type VT \_ Vector \| VT \_ UI1) o sobrescribe uno existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues:: SetBufferValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660968"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>IPortableDeviceValues:: SetBufferValue (método)

El método **SetBufferValue** agrega un nuevo valor de **byte** \* (Type VT \_ Vector \| VT \_ UI1) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
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

**Byte \*** que contiene los datos que se van a escribir en el elemento. Los datos de búfer enviados se copian en la interfaz, por lo que el autor de la llamada puede liberar este búfer después de hacer esta llamada.

</dd> <dt>

*cbValue* \[ de\]
</dt> <dd>

Tamaño del valor al que apunta *pValue*, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera adecuadamente.

No se admite el establecimiento de un valor **null** o un búfer de tamaño cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




