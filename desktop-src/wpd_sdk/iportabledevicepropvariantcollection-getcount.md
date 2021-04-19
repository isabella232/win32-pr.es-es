---
description: El método GetCount recupera el número de elementos de esta colección.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721583"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>IPortableDevicePropVariantCollection:: GetCount (método)

El método **getCount** recupera el número de elementos de esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcElems* \[ de\]
</dt> <dd>

Puntero a un **valor DWORD** que contiene el número de elementos de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**\_puntero E**</dt> </dl> | Un argumento de puntero necesario era **null**.<br/> |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método [, consulte recuperación de las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de servicio admitidos](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> <dt>

[Recuperación de las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Establecer las propiedades de varios objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




