---
description: El método CopyValuesToPropertyStore copia todos los valores de una colección en una interfaz IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: Método IPortableDeviceValues::CopyValuesToPropertyStore (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697252"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>IPortableDeviceValues::CopyValuesToPropertyStore (método)

El **método CopyValuesToPropertyStore** copia todos los valores de una colección en una **interfaz IPropertyStore.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStore* \[ En\]
</dt> <dd>

Puntero a un objeto de almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método no convierte los valores de VT \_ LPWSTR en VT \_ BSTR. Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de shell, usan la **interfaz IPropertyStore.** Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.

Este método se admite en Windows Vista y versiones posteriores de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




