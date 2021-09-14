---
description: Especifica si las redes denegadas aparecen en el Conectar a un Asistente para redes.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161160"
---
# <a name="showdeniednetwork-globalflags-element"></a>Elemento showDeniedNetwork (globalFlags)

El **elemento showDeniedNetwork** (globalFlags) especifica si las redes denegadas aparecen en el **Conectar a un asistente de** red. La directiva de grupo o la configuración de usuario pueden denegar las redes. Cuando **showDeniedNetwork tiene** el valor TRUE, las redes denegadas aparecen **en el Conectar a un asistente de** red. De lo contrario, las redes denegadas no aparecen en el asistente.

Este elemento es obligatorio. Cuando el servicio AutoConfig crea un perfil, este elemento toma el valor predeterminado false.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

El **elemento showDeniedNetwork** se define mediante el [**elemento globalFlags.**](wlan-policyschema-globalflags-wlanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




