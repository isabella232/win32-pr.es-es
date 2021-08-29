---
description: El método SetIPortableDevicePropVariantCollectionValue agrega un nuevo valor IPortableDevicePropVariantCollection (tipo VT UNKNOWN) o \_ sobrescribe uno existente.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: Método IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6f056b45e8e242dcdc88ba76764b7b6152dca58658d54e342ab3f7ea601126ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930185"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a>Método IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue

El **método SetIPortableDevicePropVariantCollectionValue** agrega un nuevo valor **IPortableDevicePropVariantCollection** (tipo VT UNKNOWN) o \_ sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que** especifica el elemento que se creará o sobrescribirá.

</dd> <dt>

*pValue* \[ En\]
</dt> <dd>

Puntero a una **interfaz IPortableDevicePropVariantCollection** que especifica el nuevo valor. El SDK copia una referencia a la interfaz enviada y llama **a AddRef** en ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Si un valor existente tiene la misma clave especificada por el parámetro *key,* sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




