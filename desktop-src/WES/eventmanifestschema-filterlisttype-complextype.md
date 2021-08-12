---
title: Tipo complejo FilterListType
description: Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Tipo complejo FilterListType EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589630"
---
# <a name="filterlisttype-complex-type"></a>Tipo complejo FilterListType

Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento    | Tipo                                                             | Descripción                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Lista de filtros.<br/> |



## <a name="remarks"></a>Comentarios

Un controlador ETW es una aplicación que llama a la [**función StartTrace**](/windows/desktop/ETW/starttrace) para crear una sesión ETW. Para obtener más información, vea [Controlar sesiones de seguimiento de eventos.](/windows/desktop/ETW/controlling-event-tracing-sessions) El controlador puede usar la [**función TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar los filtros que defina. A continuación, el controlador puede pasar uno o varios de los filtros cuando llama a la [**función EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar el proveedor. El proveedor recibe los filtros, junto con el resto de los parámetros de habilitación, en la función de devolución de llamada [*EnableCallback.*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

