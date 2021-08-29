---
title: Interfaz IResultType (WdsSharedIDL.h)
description: Expone información de tipo de propiedad.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Características heredadas del entorno de Windows IResultType
- Interfaz IResultType Características heredadas del Windows entorno , descritas
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75dd269d19af0cac7318f466a5db11e9e50ea3735594f9aa949130a439fec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014565"
---
# <a name="iresulttype-interface"></a>IResultType (interfaz)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone información de tipo de propiedad.

## <a name="members"></a>Miembros

La **interfaz IResultType** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultType** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IResultType** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso           | Descripción                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**Displayname**](-search-2x-iresulttype-displayname.md)<br/>     | Solo lectura<br/>  | Nombre para mostrar localizado del tipo:<br/>                                        |
| [**Getproperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Lectura/escritura<br/> | Esta propiedad contiene información de propiedad especificada. <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | Solo lectura<br/>  | Esta propiedad contiene la cadena utilizada para identificar el tipo en el índice. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Solo lectura<br/>  | Esta propiedad contiene el número de propiedades expuestas por el tipo . <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Solo lectura<br/>  | Esta propiedad contiene el identificador único para el tipo. <br/>                |



 

## <a name="remarks"></a>Comentarios

Estos métodos exponen los tipos de información devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

