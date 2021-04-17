---
description: El método Add agrega un elemento a la colección.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection:: Add (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708995"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>IPortableDevicePropVariantCollection:: Add (método)

El método **Add** agrega un elemento a la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValue* \[ de\]
</dt> <dd>

Puntero a un nuevo objeto **PROPVARIANT** que se va a agregar a la colección. Este método copia el **PROPVARIANT** en la colección, por lo que debe liberar la copia local de la variable llamando a **PropVariantClear** después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando VARTYPE para *pValue* es VT \_ Vector o VT \_ UI1, no se admite el establecimiento y la recuperación de un búfer **nulo** o de tamaño cero. Por ejemplo, no se permite ningún pValue. Caub. pElems = **null** ni pvalue. Caub. cElems = 0.

Si un llamador intenta agregar un elemento de otro VARTYPE incluido en la colección y el valor PROPVARIANT no se puede cambiar automáticamente mediante esta interfaz, este método producirá un error. Para cambiar el tipo de colección manualmente, llame a [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Mover contenido en el dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




