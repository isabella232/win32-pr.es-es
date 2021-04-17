---
description: El método SetIPortableDevicePropVariantCollectionValue agrega un nuevo valor de IPortableDevicePropVariantCollection (tipo VT \_ desconocido) o sobrescribe uno existente.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: 'IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 1f39ad6745dbf30df87e87be7fba358b4d9ad2c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708695"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a>IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue (método)

El método **SetIPortableDevicePropVariantCollectionValue** agrega un nuevo valor de **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (tipo VT \_ desconocido) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.

</dd> <dt>

*pValue* \[ de\]
</dt> <dd>

Puntero a una interfaz **IPortableDevicePropVariantCollection** que especifica el nuevo valor. El SDK copia una referencia a la interfaz enviada y llama a **AddRef** en ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia. La memoria de clave existente se libera adecuadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




