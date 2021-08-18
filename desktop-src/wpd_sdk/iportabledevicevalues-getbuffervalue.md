---
description: El método GetBufferValue recupera un valor de matriz de bytes (tipo VT \_ VECTOR \| VT \_ UI1) especificado por una clave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: Método IPortableDeviceValues::GetBufferValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c5d209d7ee13f55ab2236166851e2e24143b9cdeb01e947f0463491eb7446eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963704"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>IPortableDeviceValues::GetBufferValue (método)

El **método GetBufferValue** recupera un valor de matriz **de bytes** (tipo VT VECTOR VT \_ \| \_ UI1) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
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

Puntero al valor **BYTE \* *_ recuperado. El autor de la llamada es responsable de liberar la memoria mediante una llamada a _* CoTaskMemFree**.

</dd> <dt>

*pwValue* \[ out\]
</dt> <dd>

Puntero al tamaño de *ppValue*, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key no* es un **tipo BYTE.** \*<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/> |



 

## <a name="remarks"></a>Comentarios

No se admite **la recuperación** de un búfer NULL o un búfer de tamaño cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBufferValue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




