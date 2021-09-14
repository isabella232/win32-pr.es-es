---
title: Tipo complejo execType
description: Define los elementos secundarios y la información de secuenciación del elemento Exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Tipo complejo execType Programador de tareas
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259396"
---
# <a name="exectype-complex-type"></a>Tipo complejo execType

Define los elementos secundarios y la información de secuenciación del [**elemento Exec (actionGroup).**](taskschedulerschema-exec-actiongroup-element.md)

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo                                                        | Descripción                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Especifica los argumentos asociados a la operación de línea de comandos. <br/>                              |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Especifica el archivo ejecutable o el documento que se va a ejecutar.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el ejecutable.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





