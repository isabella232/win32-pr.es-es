---
description: El método GetIPortableDevicePropVariantCollectionValue recupera un valor IPortableDevicePropVariantCollection (tipo VT \_ UNKNOWN) especificado por una clave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: Método IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d0ca7f2350fee8ba5d7cea85eb19c874eb5893f86f0e17fa1b4f0e97087e7c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055195"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue (método)

El **método GetIPortableDevicePropVariantCollectionValue** recupera un valor **IPortableDevicePropVariantCollection** (tipo VT \_ UNKNOWN) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
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

Dirección de una variable que recibe un puntero a la interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperada. El autor de la llamada es responsable de **llamar a Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key no* es una **interfaz IPortableDevicePropVariantCollection.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




