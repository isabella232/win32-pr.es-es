---
description: El método GetAd recupera un elemento de la colección mediante un índice basado en cero.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721584"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>IPortableDevicePropVariantCollection:: GetAt (método)

El método **GetAd** recupera un elemento de la colección mediante un índice basado en cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

**DWORD** que contiene el índice de base cero del elemento que se va a recuperar.

</dd> <dt>

*pValue* \[ enuncia\]
</dt> <dd>

Puntero a una estructura **PROPVARIANT** . El autor de la llamada es responsable de liberar esta memoria mediante una llamada a **PropVariantClear**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                          |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Un argumento de puntero necesario era **null**.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice que se pasó estaba fuera del intervalo.<br/> |



 

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

[Recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de servicio admitidos](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> <dt>

[Recuperación de los tipos de contenido admitidos por un dispositivo](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Recuperación de las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Recuperación de los identificadores de objetos funcionales de un dispositivo](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Establecer las propiedades de varios objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




