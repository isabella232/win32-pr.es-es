---
title: Elemento ServerValidation (EapType) (PEAP)
description: Obtenga información sobre el elemento ServerValidation (EapType). Este elemento contiene información sobre cómo realizar la validación del servidor. | Elemento ServerValidation (EapType) (PEAP)
ms.assetid: 5b213853-7161-456c-bbba-d3b1118f1786
keywords:
- Elemento ServerValidation EAPHost
topic_type:
- apiref
api_name:
- ServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1495da3f1a1f5e69e7a6af9c64e69aa1ea354abc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717463"
---
# <a name="servervalidation-eaptype-element-peap"></a>Elemento ServerValidation (EapType) (PEAP)

El elemento **ServerValidation (EapType)** contiene información sobre cómo realizar la validación del servidor.

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

El elemento **ServerValidation** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

El elemento **ServerValidation** es opcional.

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

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





