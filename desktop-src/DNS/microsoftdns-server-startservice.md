---
title: Método StartService de la MicrosoftDNS_Server clase
description: El método StartService inicia el servidor DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Dns del método StartService
- Método StartService DNS , MicrosoftDNS_Server clase
- MicrosoftDNS_Server clase DNS , método StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e74de96ad24ff16ea2c2effaef78003011f5d6bd5d421336084ac5c7701f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432645"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Método StartService de la clase de servidor MicrosoftDNS \_

El **método StartService** inicia el servidor DNS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ SUCCESS indica que el servicio se inició correctamente. Cualquier otro valor es un código de error.

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

[**Método StopService de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





