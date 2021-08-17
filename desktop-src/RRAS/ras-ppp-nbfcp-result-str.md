---
title: RAS_PPP_NBFCP_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP NBFCP RESULT se usa para notificar el resultado de una operación de proyección \_ \_ de PPP \_ NetBEUI Framer (NBF) para un puerto.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT ras de estructura
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789599"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>Estructura DE \_ RESULTADOS DE RAS PPP \_ \_ NBFCP

\[La **estructura \_ DE \_ RESULTADOS NBFCP \_ de RAS PPP** no se admite desde Windows Vista.\]

La **estructura RAS PPP \_ \_ NBFCP \_ RESULT** se usa para notificar el resultado de una operación de proyección de PPP NetBEUI Framer (NBF) para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwError**
</dt> <dd>

Indica los resultados de la operación de proyección NBF. Un valor de NO ERROR indica que se ha producido correctamente, en cuyo caso, el \_ **miembro wszWksta** contiene el nombre del equipo remoto. Si la operación de proyección no se ha realizado **correctamente, dwError es** un código de error de Winerror.h o Raserror.h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignore este miembro en el servidor; solo es relevante en el cliente.

</dd> <dt>

**szName**
</dt> <dd>

Ignore este miembro en el servidor; solo es relevante en el cliente.

</dd> <dt>

**wszWksta**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el nombre NetBIOS de la estación de trabajo cliente ras.

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

 

 





