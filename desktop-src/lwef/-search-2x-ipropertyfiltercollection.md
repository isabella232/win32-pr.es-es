---
title: Interfaz IPropertyFilterCollection (WdsSharedIDL.h)
description: Expone las propiedades de la colección devuelta en función de la consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- IPropertyFilterCollection interface Legacy Windows Environment Features
- Interfaz IPropertyFilterCollection Características heredadas del entorno Windows , descritas
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
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349985"
---
# <a name="ipropertyfiltercollection-interface"></a>IPropertyFilterCollection (interfaz)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone las propiedades de la colección devuelta en función de la consulta enviada.

## <a name="members"></a>Miembros

La **interfaz IPropertyFilterCollection** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilterCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IPropertyFilterCollection** tiene estas propiedades.



| Propiedad                                                                         | Tipo de acceso           | Descripción                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Solo lectura<br/>  | Agrega un nuevo filtro a la colección. <br/>             |
| [**Claro**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Solo escritura<br/> | Borra la colección. <br/>                           |
| [**Contar**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Solo lectura<br/>  | Número de filtros de la colección. <br/>             |
| [**Getitem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lectura/escritura<br/> | Devuelve un filtro específico dentro de la colección. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Solo escritura<br/> | Quita un filtro específico de la colección. <br/>     |



 

## <a name="remarks"></a>Comentarios

Estas propiedades se usan para filtrar la colección devuelta por la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

