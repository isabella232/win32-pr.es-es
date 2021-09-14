---
description: El método SetBufferValue agrega un nuevo valor BYTE \* (tipo VT \_ VECTOR VT \| \_ UI1) o sobrescribe uno existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: Método IPortableDeviceValues::SetBufferValue (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251391"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>IPortableDeviceValues::SetBufferValue (método)

El **método SetBufferValue** agrega un nuevo valor **BYTE** \* (tipo VT VECTOR VT \_ \| \_ UI1) o sobrescribe uno existente.

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

*key* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que** especifica el elemento que se creará o sobrescribirá.

</dd> <dt>

*pValue* \[ En\]
</dt> <dd>

BYTE **\* que** contiene los datos que se escribirán en el elemento. Los datos del búfer enviados se copian en la interfaz, por lo que el autor de la llamada puede liberar este búfer después de realizar esta llamada.

</dd> <dt>

*cbValue* \[ En\]
</dt> <dd>

Tamaño del valor al que apunta *pValue*, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un valor existente tiene la misma clave especificada por el parámetro *key,* sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera correctamente.

No se admite el establecimiento de un valor **NULL** o un búfer de tamaño cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




