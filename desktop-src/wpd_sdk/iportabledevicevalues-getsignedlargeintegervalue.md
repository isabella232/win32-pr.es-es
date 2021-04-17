---
description: El método GetSignedLargeIntegerValue recupera un valor de LONGLONG (tipo VT \_ i8) especificado por una clave.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'IPortableDeviceValues:: GetSignedLargeIntegerValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680658"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a>IPortableDeviceValues:: GetSignedLargeIntegerValue (método)

El método **GetSignedLargeIntegerValue** recupera un valor de **LONGLONG** (tipo VT \_ i8) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*pValue* \[ enuncia\]
</dt> <dd>

Puntero al valor **ULong** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es un tipo **LONGLONG** .<br/> |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




