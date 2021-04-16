---
title: RAS_PPP_IPCP_RESULT estructura (rassapi. h)
description: La \_ estructura de \_ resultados de PPP de PPP de Ras \_ se utiliza para notificar el resultado de una operación de proyección de protocolo de Internet (IP) PPP para un puerto.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT de la estructura RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534264"
---
# <a name="ras_ppp_ipcp_result-structure"></a>\_Estructura de resultados de ppp ppp \_ IPCP \_

\[La estructura de **\_ \_ \_ resultados de PPP de Ras** no es compatible con Windows Vista.\]

La estructura de **\_ \_ \_ resultados de PPP de PPP de Ras** se utiliza para notificar el resultado de una operación de proyección de protocolo de Internet (IP) PPP para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwError**
</dt> <dd>

Indica los resultados de la operación de proyección IP. Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszAddress** es válido. Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Una cadena Unicode terminada en null que especifica la dirección IP asignada al cliente remoto. Esta cadena tiene el formato ****.** _b_* _._ *_c_*_._ * _d_.

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

 

 





