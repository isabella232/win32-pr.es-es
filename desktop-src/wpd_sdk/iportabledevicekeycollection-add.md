---
description: El método Add agrega una clave de propiedad a la colección.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection:: Add (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718957"
---
# <a name="iportabledevicekeycollectionadd-method"></a>IPortableDeviceKeyCollection:: Add (método)

El método **Add** agrega una clave de propiedad a la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ de de\]
</dt> <dd>

**REFPROPERTYKEY** que se va a agregar a la colección. Este método copia la clave en la colección, por lo que puede liberar la variable local después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para agregar la clave a la colección.<br/> |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [recuperar propiedades de un solo objeto](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recuperación de propiedades de objetos de contenido](retrieving-content-object-properties.md)
</dt> <dt>

[Recuperación de propiedades para un solo objeto](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Recuperación de las capacidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




