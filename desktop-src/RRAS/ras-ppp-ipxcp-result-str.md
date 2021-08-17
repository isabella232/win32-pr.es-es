---
title: RAS_PPP_IPXCP_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP IPXCP RESULT se usa para notificar el resultado de una operación de proyección de paquetes de internetwork Exchange \_ \_ PPP \_ (IPX) para un puerto.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT ras de estructura
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc79b7700fc47176928688b517377f5e02903da04841b50949937448065086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789609"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>Estructura DE \_ \_ RESULTADOs DE IPXCP de RAS PPP \_

\[La **estructura \_ DE \_ RESULTADOs IPXCP \_ de PPP ras** no se admite desde Windows Vista.\]

La **estructura RAS PPP \_ \_ IPXCP \_ RESULT** se usa para notificar el resultado de una operación de proyección de paquetes de internetwork Exchange PPP (IPX) para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwError**
</dt> <dd>

Indica los resultados de la operación de proyección IPX. Un valor de NO ERROR indica que se ha producido \_ correctamente, en cuyo caso, el **miembro wszAddress** es válido. Si la operación de proyección no se ha realizado **correctamente, dwError es** un código de error de Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica la dirección IPX asignada al cliente remoto. Esta cadena tiene ***net*.** _formulario de_ nodo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 1**](ras-port-1-str.md)
</dt> <dt>

[**RESULTADO DE \_ PROYECCIÓN DE RAS PPP \_ \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





