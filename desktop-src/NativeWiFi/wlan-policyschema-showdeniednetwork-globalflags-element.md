---
description: Especifica si las redes denegadas aparecen en el Asistente para conectarse a una red.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (Indicadores_globales)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543758"
---
# <a name="showdeniednetwork-globalflags-element"></a>Elemento showDeniedNetwork (Indicadores_globales)

El elemento **showDeniedNetwork** (indicadores_globales) especifica si las redes denegadas aparecen en el Asistente para **conectarse a una red** . La Directiva de grupo o la configuración de usuario pueden denegar las redes. Cuando **showDeniedNetwork** tiene un valor true, las redes denegadas aparecen en el Asistente para **conectarse a una red** ; de lo contrario, las redes denegadas no aparecen en el asistente.

Este elemento es obligatorio. Cuando el servicio de configuración automática crea un perfil, este elemento toma el valor predeterminado de FALSE.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

El elemento **showDeniedNetwork** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Indicadores**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Indicadores_globales (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




