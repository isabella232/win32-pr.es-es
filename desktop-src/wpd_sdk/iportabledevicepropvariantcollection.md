---
description: La interfaz IPortableDevicePropVariantCollection contiene una colección de valores PROPVARIANT indizados del mismo VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interfaz IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718723"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Interfaz IPortableDevicePropVariantCollection

La interfaz **IPortableDevicePropVariantCollection** contiene una colección de valores **PROPVARIANT** indizados del mismo VARTYPE. El VARTYPE del primer elemento que se agrega a la colección determina el VARTYPE de la colección. Se puede producir un error al intentar agregar un elemento de un VARTYPE diferente si el valor de **PROPVARIANT** no se puede cambiar al VARTYPE actual de la colección. Para cambiar el VARTYPE de la colección, llame a **ChangeType**.

Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDevicePropVariantCollection**.

## <a name="members"></a>Miembros

La interfaz **IPortableDevicePropVariantCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDevicePropVariantCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IPortableDevicePropVariantCollection** tiene estos métodos.



| Método                                                                | Descripción                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Agréguela**](iportabledevicepropvariantcollection-add.md)               | Agrega un elemento a la colección.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Convierte todos los elementos de la colección en el VARTYPE especificado.<br/>           |
| [**Claridad**](iportabledevicepropvariantcollection-clear.md)           | Libera y, a continuación, quita todos los elementos de la colección.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Recupera un elemento de la colección mediante un índice basado en cero.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Recupera el número de elementos de esta colección.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Recupera el tipo de datos de los elementos de la colección.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Quita el elemento almacenado en la ubicación especificada por el índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de colección**](collection-interfaces.md)
</dt> </dl>

 

