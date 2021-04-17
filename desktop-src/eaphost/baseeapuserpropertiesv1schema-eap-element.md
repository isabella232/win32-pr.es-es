---
title: Elemento EAP (propiedad de usuario)
description: Obtenga información sobre el elemento EAP. Este elemento captura el tipo de método seleccionado y la configuración específica del método. | Elemento EAP (propiedad de usuario)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Elemento EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717494"
---
# <a name="eap-element-user-property"></a>Elemento EAP (propiedad de usuario)

El elemento **EAP** captura el tipo de método seleccionado y la configuración específica del método.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Observaciones

El método puede definir los elementos constituyentes dentro del elemento **EAP** . El método también realiza la validación de esquemas en los elementos de **EAP**.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





