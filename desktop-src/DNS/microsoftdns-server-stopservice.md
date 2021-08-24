---
title: Método StopService de la MicrosoftDNS_Server clase
description: El método StopService detiene el servidor DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Dns del método StopService
- Método StopService DNS , MicrosoftDNS_Server clase
- MicrosoftDNS_Server clase DNS , método StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d42a443e22d382dd6e7f6ec9d528d0a1f57c6062ba0e03742033c494b75cd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076749"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Método StopService de la clase MicrosoftDNS \_ Server

El **método StopService** detiene el servidor DNS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ SUCCESS indica que el servicio se detuvo correctamente. Cualquier otro valor es un código de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ Server**](microsoftdns-server.md)
</dt> <dt>

[**Método StartService de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StartScavenging de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





