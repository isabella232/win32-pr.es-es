---
description: Especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Elemento authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082620"
---
# <a name="authperiod-onex-element"></a>Elemento authPeriod (OneX)

El elemento authPeriod (OneX) especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador. Si no se recibe una respuesta dentro del período especificado, el cliente da por supuesto que no hay ningún autenticador presente en la red.

Este elemento es opcional. Cuando authPeriod no se especifica en un perfil, se usa un valor de 18 segundos.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento **authPeriod** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> </dl>

 

 




