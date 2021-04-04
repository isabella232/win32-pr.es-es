---
description: Obtiene la versión del motor de procesamiento WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910849"
---
# <a name="getclientversion-function"></a>getClientVersion función)

Obtiene la versión del motor de procesamiento WPAD.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Cadena delimitada por signos de punto y coma que contiene direcciones IP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una lista de direcciones IP delimitadas por punto y coma ordenadas o una cadena vacía si no se puede ordenar la lista de direcciones IP.

## <a name="remarks"></a>Observaciones

Actualmente, esta función devuelve la versión 1,0.

Microsoft ha agregado esta función para permitir que los administradores de ti actualicen sus scripts de WPAD para usar versiones diferentes del motor de procesamiento WPAD sin provocar interrupciones en su implementación existente. Por ejemplo, si Microsoft ha agregado una función a la versión 2,0 del motor WPAD, los administradores pueden comprobar la versión antes de intentar llamar a esa función. Esto permite que su script funcione con las versiones 1,0 y 2,0 del motor WPAD del cliente.

## <a name="examples"></a>Ejemplos

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API de aplicación auxiliar de proxy compatible con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática de navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



