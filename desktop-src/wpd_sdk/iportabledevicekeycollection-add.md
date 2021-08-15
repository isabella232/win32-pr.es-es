---
description: El método Add agrega una clave de propiedad a la colección.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: IPortableDeviceKeyCollection::Add (método, PortableDeviceTypes.h)
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
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194725"
---
# <a name="iportabledevicekeycollectionadd-method"></a>IPortableDeviceKeyCollection::Add (Método)

El **método Add** agrega una clave de propiedad a la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que se** agregará a la colección. Este método copia la clave en la colección, por lo que puede liberar la variable local después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para agregar la clave a la colección.<br/> |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Recuperación de propiedades para un único objeto](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceKeyCollection (interfaz)**](iportabledevicekeycollection.md)
</dt> <dt>

[Recuperar propiedades content-object](retrieving-content-object-properties.md)
</dt> <dt>

[Recuperar propiedades para un solo objeto](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Recuperar las funcionalidades de representación admitidas por un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




