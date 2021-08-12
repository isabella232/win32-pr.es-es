---
title: Elemento Identity
description: Obtenga información sobre el elemento EAPHost Identity. Este elemento captura la identidad utilizada para la autenticación.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Elemento de identidad EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad88e84583be2b392ce8a4dfdaec7495f1c063fa13d4327004bfbecbc1f925ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275472"
---
# <a name="identity-element"></a>Elemento Identity

El **elemento Identity** captura la identidad utilizada para la autenticación.

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a>Comentarios

El **elemento Identity** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Server<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1 Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





