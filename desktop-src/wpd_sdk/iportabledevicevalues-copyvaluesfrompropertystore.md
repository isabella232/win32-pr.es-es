---
description: El método CopyValuesFromPropertyStore copia el contenido de un IPropertyStore en la colección.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues:: CopyValuesFromPropertyStore (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718901"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>IPortableDeviceValues:: CopyValuesFromPropertyStore (método)

El método **CopyValuesFromPropertyStore** copia el contenido de un **IPropertyStore** en la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStore* \[ de\]
</dt> <dd>

Puntero a un **IPropertyStore** que se va a copiar en la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método convierte automáticamente todos los **valores \_ BSTR de VT** en valores de **VT \_ LPWStr** .

Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de Shell, utilizan la interfaz **IPropertyStore** . Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.

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

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




