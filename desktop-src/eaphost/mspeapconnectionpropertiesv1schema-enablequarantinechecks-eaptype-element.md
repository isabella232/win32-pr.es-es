---
title: Elemento EnableQuarantineChecks (EapType)
description: Obtenga información sobre el elemento EnableQuarantineChecks (EapType). Este elemento indica si se deben realizar comprobaciones de protección de acceso a redes (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995647"
---
# <a name="enablequarantinechecks-eaptype-element"></a>Elemento EnableQuarantineChecks (EapType)

El elemento **EnableQuarantineChecks (EapType)** indica si se deben realizar comprobaciones de protección de acceso a redes (NAP).

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

El elemento **EnableQuarantineChecks** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si el elemento **EnableQuarantineChecks** es true, PEAP realizará comprobaciones de NAP; Si es FALSE, PEAP no realizará comprobaciones de NAP. El elemento **EnableQuarantineChecks** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





