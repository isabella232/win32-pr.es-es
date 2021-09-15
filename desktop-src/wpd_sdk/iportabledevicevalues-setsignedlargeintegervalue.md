---
description: El método SetSignedLargeIntegerValue agrega un nuevo valor LONGLONG (tipo VT \_ I8) o sobrescribe uno existente.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: Método IPortableDeviceValues::SetSignedLargeIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466443"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a>IPortableDeviceValues::SetSignedLargeIntegerValue (método)

El **método SetSignedLargeIntegerValue** agrega un nuevo valor **LONGLONG** (tipo VT \_ I8) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
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

LONGLONG **que** especifica el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un valor existente tiene la misma clave especificada por el parámetro *key,* sobrescribe el valor existente sin ninguna advertencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




