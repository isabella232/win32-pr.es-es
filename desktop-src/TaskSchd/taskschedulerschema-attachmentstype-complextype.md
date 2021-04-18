---
title: Tipo complejo de attachmentsType
description: Define los elementos utilizados para especificar los datos adjuntos enviados con un mensaje de correo electrónico.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- tipo complejo de attachmentsType Programador de tareas
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686104"
---
# <a name="attachmentstype-complex-type"></a>Tipo complejo de attachmentsType

Define los elementos utilizados para especificar los datos adjuntos enviados con un mensaje de correo electrónico.

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                          | Tipo                                                                    | Descripción                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Archivo**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





