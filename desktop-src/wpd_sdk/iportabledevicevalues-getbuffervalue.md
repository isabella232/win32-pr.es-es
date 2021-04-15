---
description: El método GetBufferValue recupera un valor de matriz de bytes (Type VT \_ Vector \| VT \_ UI1) especificado por una clave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'IPortableDeviceValues:: GetBufferValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709126"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>IPortableDeviceValues:: GetBufferValue (método)

El método **GetBufferValue** recupera un valor de **matriz de bytes** (Type VT \_ Vector \| VT \_ UI1) especificado por una clave.

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

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*ppValue* \[ enuncia\]
</dt> <dd>

Puntero al valor de **byte _ recuperado \* *. El autor de la llamada es responsable de liberar la memoria mediante una llamada a _* CoTaskMemFree**.

</dd> <dt>

*pcbValue* \[ enuncia\]
</dt> <dd>

Puntero al tamaño de *ppValue*, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es un tipo **byte** \* .<br/> |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

No se admite la recuperación de un búfer **nulo** ni de un búfer de tamaño cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBufferValue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




