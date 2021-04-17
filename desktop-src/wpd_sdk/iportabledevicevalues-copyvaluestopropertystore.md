---
description: El método CopyValuesToPropertyStore copia todos los valores de una colección en una interfaz IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'IPortableDeviceValues:: CopyValuesToPropertyStore (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709042"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>IPortableDeviceValues:: CopyValuesToPropertyStore (método)

El método **CopyValuesToPropertyStore** copia todos los valores de una colección en una interfaz **IPropertyStore** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStore* \[ de\]
</dt> <dd>

Puntero a un objeto de almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método no convierte valores de VT \_ LPWStr en VT \_ BSTR. Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de Shell, utilizan la interfaz **IPropertyStore** . Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.

Este método es compatible con Windows Vista y versiones posteriores de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




