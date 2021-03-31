---
title: Método StopService de la clase MicrosoftDNS_Server
description: El método StopService detiene el servidor DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- StopService (método) DNS
- Método StopService DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, StopService (método)
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
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491159"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Método StopService de la \_ clase de servidor MicrosoftDNS

El método **StopService** detiene el servidor DNS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ correcto indica que el servicio se detuvo correctamente. Cualquier otro valor es un código de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servidor MicrosoftDNS**](microsoftdns-server.md)
</dt> <dt>

[**Método StartService de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





