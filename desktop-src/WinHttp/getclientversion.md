---
description: Obtiene la versión del motor de procesamiento de WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: Función getClientVersion
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160545"
---
# <a name="getclientversion-function"></a>Función getClientVersion

Obtiene la versión del motor de procesamiento de WPAD.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Cadena delimitada por punto y coma que contiene direcciones IP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Lista de direcciones IP delimitadas por punto y coma ordenadas o una cadena vacía si no se puede ordenar la lista de direcciones IP.

## <a name="remarks"></a>Observaciones

Actualmente, esta función devuelve la versión 1.0.

Microsoft agregó esta función para permitir que los administradores de TI actualicen sus scripts de WPAD para usar diferentes versiones del motor de procesamiento de WPAD sin provocar interrupciones en su implementación existente. Por ejemplo, si Microsoft agregó una función a la versión 2.0 del motor WPAD, los administradores pueden comprobar la versión antes de intentar llamar a esa función. Esto permite que su script funcione con el cliente que ejecuta las versiones 1.0 y 2.0 del motor WPAD.

## <a name="examples"></a>Ejemplos

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API del asistente de proxy compatibles con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática del navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



