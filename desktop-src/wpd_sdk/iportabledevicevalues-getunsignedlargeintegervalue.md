---
description: El método GetUnsignedLargeIntegerValue recupera un valor ULONGLONG (tipo VT \_ UI8) especificado por una clave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: Método IPortableDeviceValues::GetUnsignedLargeIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: df10faa20094623940e9694a5612c4f49b45f3c979d7e05df3239512cb021ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194035"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>IPortableDeviceValues::GetUnsignedLargeIntegerValue (método)

El **método GetUnsignedLargeIntegerValue** recupera un valor **ULONGLONG** (tipo VT \_ UI8) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
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

Puntero al valor de **ULONGLONG recuperado.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es un **tipo ULONGLONG.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




