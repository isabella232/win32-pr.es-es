---
title: Método StartScavenging de la clase MicrosoftDNS_Server
description: El método StartScavenging inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- StartScavenging el método DNS
- Método StartScavenging DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, método StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996542"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Método StartScavenging de la \_ clase de servidor MicrosoftDNS

El método **StartScavenging** inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ correcto indica que la eliminación de registros obsoletos se ha iniciado correctamente. Cualquier otro valor es un código de error.

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

[**Método StopService de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





