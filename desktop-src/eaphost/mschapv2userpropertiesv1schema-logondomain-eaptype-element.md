---
title: Elemento LogonDomain (EapType)
description: Obtenga información sobre el elemento LogonDomain (EapType). Este elemento identifica el dominio del usuario o equipo que se va a autenticar.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078356"
---
# <a name="logondomain-eaptype-element"></a>Elemento LogonDomain (EapType)

El elemento **LogonDomain (EapType)** identifica el dominio del usuario o equipo que se va a autenticar.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

El elemento **LogonDomain** se define mediante el elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si el elemento **LogonDomain (EapType)** no está presente, se usa el dominio de Winlogon. Este elemento es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





