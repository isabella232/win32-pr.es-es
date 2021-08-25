---
description: El método SetUnsignedLargeIntegerValue agrega un nuevo valor ULONGLONG (tipo VT \_ UI8) o sobrescribe uno existente.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: Método IPortableDeviceValues::SetUnsignedLargeIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: be1f6673e4cdc5d1454c05e0df3ff43490e30e661f2b21324cf104d926f4b306
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930035"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a>IPortableDeviceValues::SetUnsignedLargeIntegerValue (método)

El **método SetUnsignedLargeIntegerValue** agrega un nuevo valor **ULONGLONG** (tipo VT \_ UI8) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
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

**ULONGLONG que** especifica el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Agregar un recurso a un objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




