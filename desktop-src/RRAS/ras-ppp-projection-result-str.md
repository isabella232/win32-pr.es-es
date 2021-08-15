---
title: RAS_PPP_PROJECTION_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP PROJECTION RESULT se usa para notificar los resultados de las distintas operaciones de \_ \_ \_ proyección PPP para un puerto.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT ras de estructura
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789589"
---
# <a name="ras_ppp_projection_result-structure"></a>Estructura DE \_ \_ RESULTADOS DE PROYECCIÓN DE RAS PPP \_

\[La **estructura RAS PPP PROJECTION \_ \_ \_ RESULT** no se admite a Windows Vista.\]

La **estructura RAS PPP PROJECTION \_ \_ \_ RESULT** se usa para notificar los resultados de las distintas operaciones de proyección PPP para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nbf**
</dt> <dd>

Estructura [**RAS \_ PPP \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md) que informa del resultado de una operación de proyección ppp NetBEUI Framer (NBF).

</dd> <dt>

**Ip**
</dt> <dd>

Estructura [**RAS \_ PPP \_ IPCP \_ RESULT**](ras-ppp-ipcp-result-str.md) que informa del resultado de una operación de proyección del Protocolo de Internet (IP) de PPP.

</dd> <dt>

**Ipx**
</dt> <dd>

Estructura [**DE \_ \_ RESULTADOs DE IPXCP \_ de PPP ras**](ras-ppp-ipxcp-result-str.md) que informa del resultado de una operación de proyección de paquetes de trabajo Exchange de trabajo de PPP (IPX).

</dd> <dt>

**at**
</dt> <dd>

Estructura [**RAS \_ PPP \_ ATCP \_ RESULT.**](ras-ppp-atcp-result-str.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura informa de los resultados de proyección para los protocolos NetBEUI, TCP/IP e IPX. Cada estructura PPP tiene un **miembro dwError** que indica si la otra información de la estructura es válida. Si **dwError** es NO \_ ERROR, la otra información es válida. Si **dwError** es uno de los códigos de error de Winerror.h o Raserror.h, la otra información no es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 1**](ras-port-1-str.md)
</dt> <dt>

[**RESULTADO \_ DE \_ ATCP de RAS PPP \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**RESULTADO \_ DE \_ IPCP DE RAS PPP \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RESULTADO \_ DE RAS PPP \_ \_ NBFCP**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





