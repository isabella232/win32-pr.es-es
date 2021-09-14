---
description: Especifica el método de transmisión utilizado para EAPOL-Start mensajes.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: elemento supplicantMode (OneX)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069444"
---
# <a name="supplicantmode-onex-element"></a>elemento supplicantMode (OneX)

El elemento supplicantMode (OneX) especifica el método de transmisión utilizado para EAPOL-Start mensajes. La siguiente tabla describe los posibles valores.



| Value               | Descripción                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| induccionesTransmission | EAPOL-Start mensajes no se transmiten. Válido solo para perfiles de LAN cableadas.                                                                                             |
| includeLearning     | El cliente determina cuándo enviar paquetes EAPOL-Start en función de la funcionalidad de red. EAPOL-Start solo se envían cuando es necesario. Válido solo para perfiles de LAN cableadas. |
| compliant           | EAPOL-Start mensajes se transmiten según lo especificado por 802.1X. Válido para perfiles de LAN cableadas e inalámbricas.                                                             |



 

Este elemento es opcional. Cuando no se especifica supplicantMode en un perfil, se usa un valor de para los `compliant` perfiles de LAN cableadas e inalámbricas.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

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

El **elemento supplicantMode** se define mediante el [**elemento OneX.**](onexschema-onex-element.md)

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

 

 




