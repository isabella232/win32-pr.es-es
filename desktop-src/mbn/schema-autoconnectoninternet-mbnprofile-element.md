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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275505"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

El elemento **AutoConnectOnInternet (MBNProfile)** especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.

Si se establece en **false**, la lógica de conexión automática del servicio de banda ancha móvil no se utilizará si hay otra conectividad de red disponible para el sistema. Si se establece en **true**, el servicio de banda ancha móvil intentará conectar automáticamente el dispositivo a la red según la configuración de conexión automática definida en el elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .

**Windows 8 y versiones posteriores:** Este elemento está en desuso. Use el método [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) con el parámetro *Property* establecido en **WCM \_ global \_ Property \_ miniMIZE \_** en su lugar.

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

El elemento **AutoConnectOnInternet** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

