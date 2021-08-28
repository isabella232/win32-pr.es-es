---
description: El método SetSignedIntegerValue agrega un nuevo valor LONG (tipo VT \_ I4) o sobrescribe uno existente.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: Método IPortableDeviceValues::SetSignedIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 71e5354c730671a4be5f344bb2503683f497003ddccecbd250490304f607e9ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704738"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a>IPortableDeviceValues::SetSignedIntegerValue (Método)

El **método SetSignedIntegerValue** agrega un nuevo valor **LONG** (tipo VT I4) o \_ sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que** especifica el elemento que se creará o sobrescribirá.

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Long **que** especifica el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Si un valor existente tiene la misma clave especificada por el parámetro *key,* sobrescribe el valor existente sin ninguna advertencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




