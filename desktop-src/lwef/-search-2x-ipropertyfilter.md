---
title: Interfaz IPropertyFilter (WdsSharedIDL.h)
description: Expone las propiedades utilizadas para filtrar la consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Características heredadas del entorno de Windows IPropertyFilter
- Interfaz IPropertyFilter Características heredadas del entorno Windows , descritas
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5bc406661492702e4a012cab58a2e0a3e08507aeaa13d10b010f14ce31e6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481099"
---
# <a name="ipropertyfilter-interface"></a>IPropertyFilter (interfaz)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone las propiedades utilizadas para filtrar la consulta.

## <a name="members"></a>Miembros

La **interfaz IPropertyFilter** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilter** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IPropertyFilter** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso           | Descripción                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lectura/escritura<br/> | Nombre de columna indizada de la propiedad por la que se filtrará. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lectura/escritura<br/> | Operador lógico que se usará al aplicar el filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lectura/escritura<br/> | Filtra la profundidad dentro de un conjunto anidado de paréntesis. <br/> |
| [**IPropertyFilter::Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lectura/escritura<br/> | Texto del filtro. <br/>                               |
| [**IPropertyFilter::UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lectura/escritura<br/> | UID de la propiedad por la que se filtrará. <br/>                 |



 

## <a name="remarks"></a>Comentarios

Estas propiedades se usan para filtrar la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

