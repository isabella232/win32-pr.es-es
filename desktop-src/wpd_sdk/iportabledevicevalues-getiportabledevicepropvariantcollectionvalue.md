---
description: El método GetIPortableDevicePropVariantCollectionValue recupera un valor de IPortableDevicePropVariantCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709220"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (método)

El método **GetIPortableDevicePropVariantCollectionValue** recupera un valor de **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
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

Dirección de una variable que recibe un puntero a la interfaz [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperada. El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es una interfaz **IPortableDevicePropVariantCollection** .<br/> |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




