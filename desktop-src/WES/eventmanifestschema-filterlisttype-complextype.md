---
title: Tipo complejo de FilterListType
description: Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359841"
---
# <a name="filterlisttype-complex-type"></a>Tipo complejo de FilterListType

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
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Una lista de filtros.<br/> |



## <a name="remarks"></a>Observaciones

Un controlador ETW es una aplicación que llama a la función [**StartTrace**](/windows/desktop/ETW/starttrace) para crear una sesión de ETW. Para obtener más información, vea [controlar las sesiones de seguimiento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions). El controlador puede usar la función [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar los filtros que se definen. Después, el controlador puede pasar uno o varios filtros cuando llama a la función [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar el proveedor. El proveedor recibe los filtros, junto con el resto de los parámetros de habilitación, en la función de devolución de llamada [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

