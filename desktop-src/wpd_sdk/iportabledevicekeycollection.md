---
description: La interfaz IPortableDeviceKeyCollection contiene una colección de valores PROPERTYKEY. Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a CoCreate con CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interfaz IPortableDeviceKeyCollection (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839395"
---
# <a name="iportabledevicekeycollection-interface"></a>IPortableDeviceKeyCollection (interfaz)

La **interfaz IPortableDeviceKeyCollection** contiene una colección de **valores PROPERTYKEY.** Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceKeyCollection**.

## <a name="members"></a>Miembros

La **interfaz IPortableDeviceKeyCollection** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceKeyCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IPortableDeviceKeyCollection** tiene estos métodos.



| Método                                                    | Descripción                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Añadir**](iportabledevicekeycollection-add.md)           | Agrega una clave de propiedad a la colección.<br/>                                   |
| [**Borrar**](iportabledevicekeycollection-clear.md)       | Elimina todos los elementos de la colección.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Recupera un **PROPERTYKEY de** la colección por índice.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Recupera el número de claves de esta colección.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Quita el elemento almacenado en la ubicación especificada por el índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de colección**](collection-interfaces.md)
</dt> </dl>

 

