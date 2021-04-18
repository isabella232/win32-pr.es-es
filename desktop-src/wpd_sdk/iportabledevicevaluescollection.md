---
description: La interfaz IPortableDeviceValuesCollection contiene una colección de interfaces IPortableDeviceValues indizadas basadas en cero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interfaz IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718628"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interfaz IPortableDeviceValuesCollection

La interfaz **IPortableDeviceValuesCollection** contiene una colección de interfaces **IPortableDeviceValues** indizadas basadas en cero. Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Miembros

La interfaz **IPortableDeviceValuesCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValuesCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IPortableDeviceValuesCollection** tiene estos métodos.



| Método                                                       | Descripción                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Agréguela**](iportabledevicevaluescollection-add.md)           | Agrega un elemento a la colección.<br/>                                           |
| [**Claridad**](iportabledevicevaluescollection-clear.md)       | Libera todos los elementos de la colección.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Recupera un elemento de la colección mediante un índice basado en cero.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Recupera el número de elementos de la colección.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Quita el elemento almacenado en la ubicación especificada por el índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de colección**](collection-interfaces.md)
</dt> </dl>

 

