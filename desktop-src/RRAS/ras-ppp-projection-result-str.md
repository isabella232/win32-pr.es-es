---
title: RAS_PPP_PROJECTION_RESULT estructura (rassapi. h)
description: La \_ estructura del \_ resultado de la proyección PPP \_ de Ras se utiliza para notificar los resultados de las distintas operaciones de proyección de PPP para un puerto.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT de la estructura RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802497"
---
# <a name="ras_ppp_projection_result-structure"></a>Estructura del resultado de la \_ proyección PPP de Ras \_ \_

\[La estructura del resultado de la **\_ \_ proyección \_ PPP de Ras** no es compatible con Windows Vista.\]

La estructura del resultado de la **\_ \_ proyección \_ PPP de Ras** se utiliza para notificar los resultados de las distintas operaciones de proyección de PPP para un puerto.

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

Una estructura de [**\_ \_ \_ resultado PPP NBFCP de Ras**](ras-ppp-nbfcp-result-str.md) que informa del resultado de una operación de proyección de PPP NetBEUI Framer (NBF).

</dd> <dt>

**intelectual**
</dt> <dd>

Una estructura de [**\_ \_ \_ resultados de PPP de PPP de Ras**](ras-ppp-ipcp-result-str.md) que informa del resultado de una operación de proyección del Protocolo de Internet (IP) de PPP.

</dd> <dt>

**requerir**
</dt> <dd>

Una estructura de [**\_ \_ \_ resultado de IPXCP PPP de Ras**](ras-ppp-ipxcp-result-str.md) que informa del resultado de una operación de proyección de intercambio de paquetes en la red (IPX) de PPP.

</dd> <dt>

**at**
</dt> <dd>

Una estructura de [**\_ \_ \_ resultado PPP ATCP de Ras**](ras-ppp-atcp-result-str.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura notifica los resultados de proyección para los protocolos NetBEUI, TCP/IP y IPX. Cada estructura PPP tiene un miembro **dwError** que indica si la otra información de la estructura es válida. Si **dwError** NO es un \_ error, la otra información es válida. Si **dwError** es uno de los códigos de error de Winerror. h o Raserror. h, la otra información no es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Puerto ras \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_resultado de PPP \_ ATCP \_ de Ras**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**resultado de PPP de PPP de RAS \_ \_ \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**\_resultado de \_ IPXCP de PPP de Ras \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_resultado de \_ NBFCP de PPP de Ras \_**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





