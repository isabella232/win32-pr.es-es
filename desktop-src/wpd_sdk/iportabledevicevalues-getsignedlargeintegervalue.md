---
description: El método GetSignedLargeIntegerValue recupera un valor LONGLONG (tipo VT \_ I8) especificado por una clave.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: Método IPortableDeviceValues::GetSignedLargeIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 516d7c08b68e4480b3240ea9335793589114070859cf28d5cf91e645b616a2db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055115"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a>IPortableDeviceValues::GetSignedLargeIntegerValue (método)

El **método GetSignedLargeIntegerValue** recupera un valor **LONGLONG** (tipo VT \_ I8) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
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

Puntero al valor **de ULONG** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key no* es un **tipo LONGLONG.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




