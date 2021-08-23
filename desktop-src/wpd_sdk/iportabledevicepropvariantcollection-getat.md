---
description: 'Método IPortableDevicePropVariantCollection::GetAt: el método GetAt recupera un elemento de la colección mediante un índice de base cero.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: IPortableDevicePropVariantCollection::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 02fa273b3bedea78884e15d2dedb5b7d2f675c78330c735e3bfb1896bc9d5199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963734"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>IPortableDevicePropVariantCollection::GetAt (método)

El **método GetAt** recupera un elemento de la colección mediante un índice de base cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ En\]
</dt> <dd>

**DWORD** que contiene el índice de base cero del elemento que se recuperará.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Puntero a una **estructura PROPVARIANT.** El autor de la llamada es responsable de liberar esta memoria mediante una **llamada a PropVariantClear**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                          |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | Un argumento de puntero necesario era **NULL.**<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice que se pasó estaba fuera del intervalo.<br/> |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Recuperación de las categorías funcionales admitidas por un dispositivo.](retrieving-the-functional-categories-supported-by-a-device.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperar formatos de servicio admitidos](retrieving-supported-formats.md)
</dt> <dt>

[Recuperar métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> <dt>

[Recuperar los tipos de contenido admitidos por un dispositivo](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Recuperar las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Recuperar los identificadores de objeto funcional de un dispositivo](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Recuperar las funcionalidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Establecer propiedades para varios objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




