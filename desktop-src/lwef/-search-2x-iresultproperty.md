---
title: Interfaz IResultProperty (WdsSharedIDL. h)
description: Expone las propiedades de los resultados.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Interfaz IResultProperty características del entorno heredado de Windows
- Interfaz IResultProperty características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695972"
---
# <a name="iresultproperty-interface"></a>Interfaz IResultProperty

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone las propiedades de los resultados.

## <a name="members"></a>Miembros

La interfaz **IResultProperty** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultProperty** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IResultProperty** tiene estos métodos.



| Método                                                    | Descripción                 |
|:----------------------------------------------------------|:----------------------------|
| [**Goback**](-search-2x-iresultproperty-goback.md)       | Sin implementar.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Sin implementar.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IResultProperty** tiene estas propiedades.



| Propiedad                                                                   | Tipo de acceso          | Descripción                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Tipo**](-search-2x-iresultproperty-datatype.md)<br/>         | Solo lectura<br/> | Un tipo de datos de propiedades. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Solo lectura<br/> | Nombre para mostrar localizado de la propiedad. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Solo lectura<br/> | Visability de la propiedad. <br/>               |
| [**Diversas**](-search-2x-iresultproperty-hint.md)<br/>                 | Solo lectura<br/> | Valor especial que se usa para ayudar a la recuperación de datos. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Solo lectura<br/> | Nombre de la columna de propiedades en el índice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Solo lectura<br/> | Identificador único de la propiedad. <br/>       |



 

## <a name="remarks"></a>Observaciones

Estas son las propiedades de los elementos devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

