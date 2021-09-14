---
description: Especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168154"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

El **elemento AutoConnectOnInternet (MBNProfile)** especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.

Si se establece en **FALSE**, la lógica de conexión automática del servicio banda ancha móvil no se usará si hay alguna otra conectividad de red disponible para el sistema. Si se establece en **TRUE,** el servicio banda ancha móvil intentará conectar automáticamente el dispositivo a la red en función de la configuración de conexión automática definida en el [**elemento ConnectionMode.**](schema-connectionmode-mbnprofile-element.md)

**Windows 8 y versiones posteriores:** Este elemento está en desuso. Use el [**método WcmSetProperty con el**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) parámetro *Property* establecido en **wcm global property minimize \_ policy en su \_ \_ \_ lugar.**

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

El **elemento AutoConnectOnInternet** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

