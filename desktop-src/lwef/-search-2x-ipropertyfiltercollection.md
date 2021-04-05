---
title: Interfaz IPropertyFilterCollection (WdsSharedIDL. h)
description: Expone las propiedades de la colección devuelta basándose en la consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359769"
---
# <a name="ipropertyfiltercollection-interface"></a>Interfaz IPropertyFilterCollection

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone las propiedades de la colección devuelta basándose en la consulta enviada.

## <a name="members"></a>Miembros

La interfaz **IPropertyFilterCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilterCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IPropertyFilterCollection** tiene estas propiedades.



| Propiedad                                                                         | Tipo de acceso           | Descripción                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Solo lectura<br/>  | Agrega un nuevo filtro a la colección. <br/>             |
| [**claridad**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Solo escritura<br/> | Borra la colección. <br/>                           |
| [**Contabiliza**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Solo lectura<br/>  | Número de filtros de la colección. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lectura/escritura<br/> | Devuelve un filtro específico dentro de la colección. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Solo escritura<br/> | Quita un filtro específico de la colección. <br/>     |



 

## <a name="remarks"></a>Observaciones

Estas propiedades se usan para filtrar la colección devuelta por la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

