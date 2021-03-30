---
title: Interfaz IPropertyFilter (WdsSharedIDL. h)
description: Expone propiedades utilizadas para filtrar la consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Interfaz IPropertyFilter características del entorno heredado de Windows
- Interfaz IPropertyFilter características del entorno heredado de Windows, descritas
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
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534696"
---
# <a name="ipropertyfilter-interface"></a>Interfaz IPropertyFilter

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone propiedades utilizadas para filtrar la consulta.

## <a name="members"></a>Miembros

La interfaz **IPropertyFilter** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilter** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IPropertyFilter** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso           | Descripción                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lectura/escritura<br/> | Nombre de columna indizada de la propiedad por la que se va a filtrar. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lectura/escritura<br/> | Operador lógico que se va a usar al aplicar el filtro. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lectura/escritura<br/> | Filtra la profundidad dentro de un conjunto anidado de paréntesis. <br/> |
| [**IPropertyFilter:: Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lectura/escritura<br/> | Texto del filtro. <br/>                               |
| [**IPropertyFilter:: UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lectura/escritura<br/> | UID de la propiedad por la que se va a filtrar. <br/>                 |



 

## <a name="remarks"></a>Observaciones

Estas propiedades se usan para filtrar la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

