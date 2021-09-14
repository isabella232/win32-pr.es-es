---
title: RAS_PPP_ATCP_RESULT estructura (Rassapi.h)
description: La estructura RAS PPP ATCP RESULT se usa para notificar el resultado de una operación de proyección \_ \_ del protocolo \_ AppleTalk para un puerto.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT ras de estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073870"
---
# <a name="ras_ppp_atcp_result-structure"></a>Estructura DE \_ \_ RESULTADOS ATCP de RAS PPP \_

\[La **estructura RAS PPP \_ \_ ATCP \_ RESULT** no se admite a Windows Vista.\]

La **estructura RAS PPP \_ \_ ATCP \_ RESULT** se usa para notificar el resultado de una operación de proyección del protocolo AppleTalk para un puerto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Especifica un valor que indica los resultados de la operación de proyección de AppleTalk. Un valor de NO ERROR indica que se ha producido \_ correctamente, en cuyo caso, el **miembro wszAddress** es válido. Si la operación de proyección no se realiza **correctamente, dwError es** un código de error de Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Especifica una cadena Unicode terminada en NULL que especifica la dirección IP asignada al cliente remoto.

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

[**RESULTADO DE \_ PROYECCIÓN DE RAS PPP \_ \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





