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
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466461"
---
# <a name="iportabledevicekeycollection-interface"></a>IPortableDeviceKeyCollection (interfaz)

La **interfaz IPortableDeviceKeyCollection** contiene una colección de **valores PROPERTYKEY.** Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceKeyCollection**.

## <a name="members"></a>Members

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

 

