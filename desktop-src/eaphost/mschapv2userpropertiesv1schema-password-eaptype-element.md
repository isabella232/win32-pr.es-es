---
title: Password (EapType), elemento
description: Obtenga información sobre el elemento Password (EapType). Este elemento identifica la contraseña del usuario o equipo que se autentica.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078386"
---
# <a name="password-eaptype-element"></a>Password (EapType), elemento

El elemento **password (EapType)** identifica la contraseña del usuario o equipo que se va a autenticar.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

El elemento de **contraseña** se define mediante el elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si el elemento **password (EapType)** no está presente, el hash de contraseña se obtiene de Winlogon. Este elemento es opcional.

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

 

 





