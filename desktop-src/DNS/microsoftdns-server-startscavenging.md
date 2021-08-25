---
title: Método StartScavenging de la MicrosoftDNS_Server clase
description: El método StartScavenging inicia la búsqueda de registros obsoletos en las zonas sujetas a scavenging.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- StartScavenging method DNS
- Método StartScavenging DNS , MicrosoftDNS_Server clase
- MicrosoftDNS_Server clase DNS , método StartScavenging
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
ms.openlocfilehash: b6173021ca49dc73b7ec89f60b097b2179078a774c9a40c26fda2c41b2ad25f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874775"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Método StartScavenging de la clase de servidor MicrosoftDNS \_

El **método StartScavenging** inicia la búsqueda de registros obsoletos en las zonas sujetas a scavenging.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

ERROR \_ SUCCESS indica que la búsqueda se inició correctamente. Cualquier otro valor es un código de error.

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

[**Método StopService de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de servidor MicrosoftDNS \_**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





