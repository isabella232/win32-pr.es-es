---
title: RAS_SERVER_0 estructura (Rassapi.h)
description: La función \_ RasAdminServerGetInfo usa la estructura RAS SERVER 0 para devolver información sobre los puertos \_ configurados en un servidor RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 ras de estructura
- PRAS_SERVER_0 ras de puntero de estructura
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476638"
---
# <a name="ras_server_0-structure"></a>Estructura \_ RAS SERVER \_ 0

\[La **estructura RAS SERVER \_ \_ 0** no se admite a partir Windows Vista.\]

La función [**RasAdminServerGetInfo**](rasadminservergetinfo.md) usa la estructura **RAS \_ SERVER \_ 0** para devolver información sobre los puertos configurados en un servidor RAS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Members

<dl> <dt>

**TotalPorts**
</dt> <dd>

Especifica el número total de puertos configurados en el servidor RAS que están disponibles para que los clientes remotos se conecten. Por ejemplo, si el número total de puertos configurados para el acceso telefónico a un servidor es cuatro, pero uno de los puertos está actualmente en uso para marcar, **TotalPorts** es tres.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Especifica el número de puertos actualmente en uso por los clientes remotos.

</dd> <dt>

**RasVersion**
</dt> <dd>

Especifica la versión del servidor RAS. Use esta información para realizar acciones específicas de la versión. Este miembro es uno de los siguientes valores.



| Value                                                                                                                                                                  | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica un servidor RAS de la versión 1.0 de LAN Manager.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica un servidor Windows NT Server 3.51 y un cliente o servidor RAS anterior.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ CURRENT**</dt> </dl> | Indica un cliente Windows o servidor RAS nt 4.0.<br/>                     |



 

</dd> </dl>

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

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





