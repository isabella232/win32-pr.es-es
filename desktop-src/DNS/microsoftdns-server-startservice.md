---
title: Método StartService de la clase MicrosoftDNS_Server
description: El método StartService inicia el servidor DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS del método StartService
- Método StartService DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, StartService
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
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658223"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Método StartService de la \_ clase de servidor MicrosoftDNS

El método **StartService** inicia el servidor DNS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ correcto indica que el servicio se ha iniciado correctamente. Cualquier otro valor es un código de error.

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

[**Método StopService de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





