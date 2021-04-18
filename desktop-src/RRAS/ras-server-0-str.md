---
title: RAS_SERVER_0 estructura (rassapi. h)
description: '\_ \_ La función RasAdminServerGetInfo utiliza la estructura del servidor RAS 0 para devolver información acerca de los puertos configurados en un servidor RAS.'
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 de la estructura RAS
- PRAS_SERVER_0 de puntero de estructura RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651408"
---
# <a name="ras_server_0-structure"></a>\_Estructura del servidor RAS \_ 0

\[La estructura del **\_ servidor RAS \_ 0** no es compatible con Windows Vista.\]

La función [**RasAdminServerGetInfo**](rasadminservergetinfo.md) utiliza la estructura del **\_ servidor RAS \_ 0** para devolver información acerca de los puertos configurados en un servidor RAS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TotalPorts**
</dt> <dd>

Especifica el número total de puertos configurados en el servidor RAS que están disponibles para que los clientes remotos se conecten a. Por ejemplo, si el número total de puertos configurados para el acceso telefónico a un servidor es cuatro, pero uno de los puertos se está usando actualmente para el marcado, **TotalPorts** es tres.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Especifica el número de puertos actualmente en uso por los clientes remotos.

</dd> <dt>

**RasVersion**
</dt> <dd>

Especifica la versión del servidor RAS. Use esta información para realizar una acción específica de la versión. Este miembro es uno de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica un servidor RAS de LAN Manager versión 1,0.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica un servidor o cliente RAS de Windows NT Server 3,51 y versiones anteriores.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ actual**</dt> </dl> | Indica un servidor o cliente RAS de Windows NT 4,0.<br/>                     |



 

</dd> </dl>

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

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





