---
title: Interfaz IResultType (WdsSharedIDL. h)
description: Expone información de tipo de propiedad.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Interfaz IResultType características del entorno heredado de Windows
- Interfaz IResultType características del entorno heredado de Windows, descritas
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
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490019"
---
# <a name="iresulttype-interface"></a>Interfaz IResultType

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone información de tipo de propiedad.

## <a name="members"></a>Miembros

La interfaz **IResultType** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultType** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IResultType** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso           | Descripción                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresulttype-displayname.md)<br/>     | Solo lectura<br/>  | Nombre para mostrar localizado del tipo:<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Lectura/escritura<br/> | Esta propiedad contiene información de propiedad especificada. <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | Solo lectura<br/>  | Esta propiedad contiene la cadena que se usa para identificar el tipo en el índice. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Solo lectura<br/>  | Esta propiedad contiene el número de propiedades expuestas por el tipo. <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Solo lectura<br/>  | Esta propiedad contiene el identificador único para el tipo. <br/>                |



 

## <a name="remarks"></a>Observaciones

Estos métodos exponen los tipos de información devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

