---
description: El método ChangeType convierte todos los elementos de la colección en el VARTYPE especificado.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: Método IPortableDevicePropVariantCollection::ChangeType (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839335"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>IPortableDevicePropVariantCollection::ChangeType (Método)

El **método ChangeType** convierte todos los elementos de la colección en el VARTYPE especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vt* \[ En\]
</dt> <dd>

Especifica el **VARTYPE en** el que desea convertir todos los elementos de la colección. Entre los tipos de ejemplo se incluyen VT \_ UI4 y VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Si se produce un error en este método, la colección puede quedar en un estado intermedio, con algunos miembros convertidos y otros no convertidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




