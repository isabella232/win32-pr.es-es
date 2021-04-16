---
description: El método GetErrorValue recupera un valor HRESULT (tipo VT \_ error) especificado por una clave.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'IPortableDeviceValues:: GetErrorValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649830"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a>IPortableDeviceValues:: GetErrorValue (método)

El método **GetErrorValue** recupera un valor **HRESULT** (tipo VT \_ error) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
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

Puntero al valor **HRESULT** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es un tipo **HRESULT** .<br/> |
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

[**IPortableDeviceValues::SetErrorValue**](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




