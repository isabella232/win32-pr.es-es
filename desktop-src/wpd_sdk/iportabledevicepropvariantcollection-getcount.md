---
description: El método GetCount recupera el número de elementos de esta colección.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: IPortableDevicePropVariantCollection::GetCount (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2b82ce3c916df3603478888ecdc388e80ee4b4d635a25b238f9ba6a03ef61901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055205"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>IPortableDevicePropVariantCollection::GetCount (método)

El **método GetCount** recupera el número de elementos de esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcElems* \[ En\]
</dt> <dd>

Puntero a un **DWORD** que contiene el número de elementos de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Un argumento de puntero necesario era **NULL.**<br/> |



 

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

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperar formatos de servicio admitidos](retrieving-supported-formats.md)
</dt> <dt>

[Recuperar métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> <dt>

[Recuperar las categorías funcionales admitidas por un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Establecer propiedades para varios objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




