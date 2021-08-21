---
title: Interfaz IResultProperty (WdsSharedIDL.h)
description: Expone las propiedades de resultado.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Características heredadas del entorno de Windows IResultProperty
- Interfaz IResultProperty características heredadas Windows entorno , descritas
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
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754588"
---
# <a name="iresultproperty-interface"></a>Interfaz IResultProperty

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone las propiedades de resultado.

## <a name="members"></a>Miembros

La **interfaz IResultProperty** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultProperty** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IResultProperty** tiene estos métodos.



| Método                                                    | Descripción                 |
|:----------------------------------------------------------|:----------------------------|
| [**Goback**](-search-2x-iresultproperty-goback.md)       | Sin implementar.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Sin implementar.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IResultProperty** tiene estas propiedades.



| Propiedad                                                                   | Tipo de acceso          | Descripción                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Datatype**](-search-2x-iresultproperty-datatype.md)<br/>         | Solo lectura<br/> | Tipo de datos properties. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Solo lectura<br/> | Nombre para mostrar localizado de la propiedad. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Solo lectura<br/> | Visibilidad de la propiedad. <br/>               |
| [**Pista**](-search-2x-iresultproperty-hint.md)<br/>                 | Solo lectura<br/> | Valor especial que se usa para facilitar la recuperación de datos. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Solo lectura<br/> | Nombre de columna de propiedades en el índice. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Solo lectura<br/> | Identificador único de la propiedad. <br/>       |



 

## <a name="remarks"></a>Comentarios

Estos son los elementos que devuelven propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

