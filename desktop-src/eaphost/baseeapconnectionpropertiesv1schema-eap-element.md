---
title: Elemento EAP (propiedades de conexión)
description: Obtenga información sobre el elemento EAP. Este elemento captura el tipo de método seleccionado y la configuración específica del método. | Elemento EAP (propiedades de conexión)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698066"
---
# <a name="eap-element-connection-properties"></a>Elemento EAP (propiedades de conexión)

El elemento **EAP** captura el tipo de método seleccionado y la configuración específica del método.

``` syntax
<xs:element name="Eap
          
        "
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

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





