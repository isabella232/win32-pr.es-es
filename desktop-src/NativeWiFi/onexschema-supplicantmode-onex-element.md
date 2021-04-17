---
description: Especifica el método de transmisión utilizado para los mensajes de EAPOL-Start.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677748"
---
# <a name="supplicantmode-onex-element"></a>Elemento supplicantMode (OneX)

El elemento supplicantMode (OneX) especifica el método de transmisión que se usa para los mensajes de EAPOL-Start. La siguiente tabla describe los posibles valores.



| Value               | Descripción                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibitTransmission | No se transmiten los mensajes de EAPOL-Start. Válido solo para perfiles de LAN con cable.                                                                                             |
| includeLearning     | El cliente determina cuándo se deben enviar los paquetes de EAPOL-Start en función de la capacidad de la red. EAPOL-Start mensajes solo se envían cuando es necesario. Válido solo para perfiles de LAN con cable. |
| compliant           | EAPOL-Start mensajes se transmiten según lo especificado por 802.1 X. Válido para perfiles de LAN inalámbrica y cableada.                                                             |



 

Este elemento es opcional. Cuando supplicantMode no se especifica en un perfil, se usa un valor de `compliant` para los perfiles de LAN inalámbrica y cableada.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento **supplicantMode** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .

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

 

 




