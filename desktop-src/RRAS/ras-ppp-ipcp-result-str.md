---
title: RAS_PPP_IPCP_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP IPCP RESULT se usa para notificar el resultado de una operación de proyección del Protocolo \_ \_ de Internet \_ (IP) de PPP para un puerto.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT ras de estructura
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073863"
---
# <a name="ras_ppp_ipcp_result-structure"></a>Estructura DE \_ \_ RESULTADOS DE IPCP de RAS PPP \_

\[La **estructura RAS PPP \_ \_ IPCP \_ RESULT** no se admite desde Windows Vista.\]

La **estructura RAS PPP \_ \_ IPCP \_ RESULT** se usa para notificar el resultado de una operación de proyección del Protocolo de Internet (IP) de PPP para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Indica los resultados de la operación de proyección IP. Un valor de NO ERROR indica que se ha producido \_ correctamente, en cuyo caso, el **miembro wszAddress** es válido. Si la operación de proyección no se ha realizado **correctamente, dwError es** un código de error de Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica la dirección IP asignada al cliente remoto. Esta cadena tiene el formato ****.** _b_* _._ *_c_*_._ * _d_.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





