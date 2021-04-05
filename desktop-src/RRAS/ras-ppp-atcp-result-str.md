---
title: RAS_PPP_ATCP_RESULT estructura (rassapi. h)
description: La \_ estructura de \_ \_ resultados de PPP de PPP de Ras se utiliza para notificar el resultado de una operación de proyección de protocolo AppleTalk para un puerto.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996498"
---
# <a name="ras_ppp_atcp_result-structure"></a>\_Estructura de \_ \_ resultado PPP de protocolo ras

\[La estructura de **\_ \_ \_ resultados de PPP de protocolo ras** no es compatible con Windows Vista.\]

La estructura de **\_ \_ \_ resultados de PPP de PPP de Ras** se utiliza para notificar el resultado de una operación de proyección de protocolo AppleTalk para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwError**
</dt> <dd>

Especifica un valor que indica los resultados de la operación de proyección de AppleTalk. Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszAddress** es válido. Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Especifica una cadena Unicode terminada en null que especifica la dirección IP asignada al cliente remoto.

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

[**\_resultado de \_ proyección \_ PPP de Ras**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





