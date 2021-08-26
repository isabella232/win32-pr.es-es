---
description: 'Método IPortableDevicePropVariantCollection::Add: el método Add agrega un elemento a la colección.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: IPortableDevicePropVariantCollection::Add (método, PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fd90e4702045200e4f2766f6dcdd661ff83b6cd3370970a22e3211eebfa13c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055265"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>IPortableDevicePropVariantCollection::Add (Método)

El **método Add** agrega un elemento a la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* \[ En\]
</dt> <dd>

Puntero a un nuevo **objeto PROPVARIANT** que se agregará a la colección. Este método copia **PROPVARIANT** en la colección, por lo que debe liberar la copia local de la variable llamando a **PropVariantClear** después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando VARTYPE para *pValue* es VT VECTOR o VT UI1, no se admite la configuración y recuperación de un búfer null \_ \_ o de tamaño cero.  Por ejemplo, no se permiten pValue.caub.pElems = **NULL** ni pValue.caub.cElems = 0.

Si un autor de la llamada intenta agregar un elemento de otro VARTYPE contenido en la colección y esta interfaz no puede cambiar automáticamente el valor PROPVARIANT, se producirá un error en este método. Para cambiar el tipo de colección manualmente, llame a [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Recuperación de un identificador de objeto a partir de un identificador único persistente.](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Mover contenido en el dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




