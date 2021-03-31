---
title: Elemento UseWinLogonCredentials (EapType)
description: Obtenga información sobre el elemento UseWinLogonCredentials (EapType). Este elemento controla el uso de las credenciales de WinLogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793929"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

El elemento **UseWinLogonCredentials (EapType)** controla el uso de las credenciales de WinLogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

El elemento **UseWinLogonCredentials** se define mediante el elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si es TRUE, EAP MS-CHAPv2 obtiene las credenciales de Winlogon. Si es FALSE, EAP MS-CHAPv2 obtiene las credenciales del usuario. El elemento **UseWinLogonCredentials (EapType)** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versiones mínimas admitidas del sistema operativo |
|------|-------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





