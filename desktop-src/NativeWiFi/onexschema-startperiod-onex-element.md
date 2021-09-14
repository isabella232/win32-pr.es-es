---
description: Especifica el período de tiempo, en segundos, que se debe esperar antes de EAPOL-Start se envía una aplicación.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069445"
---
# <a name="startperiod-onex-element"></a>elemento startPeriod (OneX)

El elemento startPeriod (OneX) especifica el tiempo, en segundos, que se debe esperar antes de que se envíe EAPOL-Start una aplicación. Se EAPOL-Start mensaje para iniciar el proceso de autenticación 802.1X.

Este elemento es opcional. Cuando startPeriod no se especifica en un perfil, se usa un valor de 5 segundos.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="startPeriod">
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

El **elemento startPeriod** se define mediante el [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




