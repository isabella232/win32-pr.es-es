---
title: Username (elemento) (CHAP)
description: Obtenga información sobre el elemento username, que identifica al usuario que se está autenticando. Vea un ejemplo de sintaxis y vea más recursos disponibles.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Username (elemento) EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995629"
---
# <a name="username-element-chap"></a>Username (elemento) (CHAP)

El elemento **username** identifica el usuario que se va a autenticar.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>Observaciones

Si el elemento **username** no está presente, el nombre de usuario se obtiene de Winlogon. Este elemento es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





