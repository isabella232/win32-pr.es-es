---
title: RAS_PPP_PROJECTION_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP PROJECTION RESULT se usa para informar de los resultados de las distintas operaciones de \_ \_ \_ proyección de PPP para un puerto.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT estructura RAS
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
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476639"
---
# <a name="ras_ppp_projection_result-structure"></a>Estructura DE \_ \_ RESULTADOS DE PROYECCIÓN DE RAS PPP \_

\[La **estructura RAS PPP PROJECTION \_ \_ \_ RESULT** no se admite desde Windows Vista.\]

La **estructura RAS PPP PROJECTION \_ \_ \_ RESULT** se usa para informar de los resultados de las distintas operaciones de proyección de PPP para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**nbf**
</dt> <dd>

Estructura [**RAS \_ PPP \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md) que informa del resultado de una operación de proyección de PPP NetBEUI Framer (NBF).

</dd> <dt>

**Ip**
</dt> <dd>

Estructura [**RAS \_ PPP \_ IPCP \_ RESULT**](ras-ppp-ipcp-result-str.md) que informa del resultado de una operación de proyección de Protocolo de Internet (IP) de PPP.

</dd> <dt>

**Ipx**
</dt> <dd>

Estructura [**RAS \_ PPP \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md) que informa del resultado de una operación de proyección de paquetes de trabajo Exchange ppp (IPX).

</dd> <dt>

**at**
</dt> <dd>

Estructura [**DE \_ \_ RESULTADOS ATCP \_ de RAS PPP.**](ras-ppp-atcp-result-str.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura informa de los resultados de proyección para los protocolos NetBEUI, TCP/IP e IPX. Cada estructura PPP tiene un **miembro dwError** que indica si la otra información de la estructura es válida. Si **dwError** es NO \_ ERROR, la otra información es válida. Si **dwError es** uno de los códigos de error de Winerror.h o Raserror.h, la otra información no es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS \_ PPP \_ ATCP \_ RESULT**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**RESULTADO \_ DE \_ IPCP DE RAS PPP \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RESULTADO \_ DE RAS PPP \_ NBFCP \_**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





