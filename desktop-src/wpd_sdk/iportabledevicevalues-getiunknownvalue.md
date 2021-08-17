---
description: El método GetIUnknownValue recupera un valor de interfaz IUnknown (tipo VT \_ UNKNOWN) especificado por una clave.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: Método IPortableDeviceValues::GetIUnknownValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: daf1164fefdc414a84508e4b295620af3cb671e9da624dd60cc08541c5c4fd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963654"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>IPortableDeviceValues::GetIUnknownValue (método)

El **método GetIUnknownValue** recupera un valor de interfaz **IUnknown** (tipo VT \_ UNKNOWN) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
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

Dirección de una variable que recibe un puntero a la **interfaz IUnknown recuperada.** El autor de la llamada es responsable de **llamar a Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                             |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es una **interfaz IUnknown.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




