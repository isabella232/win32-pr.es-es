---
title: RAS_PPP_NBFCP_RESULT estructura (rassapi. h)
description: La \_ estructura de resultados NBFCP de PPP de Ras \_ \_ se usa para informar del resultado de una operación de proyección de PPP NetBEUI Framer (NBF) para un puerto.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT de la estructura RAS
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
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150392"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>\_Estructura de \_ resultado de NBFCP de PPP de Ras \_

\[La estructura de **\_ \_ \_ resultados NBFCP de PPP de Ras** no es compatible con Windows Vista.\]

La estructura de **\_ \_ \_ resultados NBFCP de PPP de Ras** se usa para informar del resultado de una operación de proyección de PPP NetBEUI Framer (NBF) para un puerto.

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

Indica los resultados de la operación de proyección de NBF. Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszWksta** contiene el nombre del equipo remoto. Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Omitir este miembro en el servidor; solo es relevante en el cliente.

</dd> <dt>

**szName**
</dt> <dd>

Omitir este miembro en el servidor; solo es relevante en el cliente.

</dd> <dt>

**wszWksta**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el nombre NetBIOS de la estación de trabajo del cliente RAS.

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

[**\_Puerto ras \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_resultado de \_ proyección \_ PPP de Ras**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





