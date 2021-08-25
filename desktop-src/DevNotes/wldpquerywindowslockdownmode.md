---
description: Recupera el modo seguro Windows actual. Windows puede estar en modo bloqueado, en modo normal desbloqueado o en modo de prueba.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Función WldpQueryWindowsLockdownMode (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911295"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Función WldpQueryWindowsLockdownMode

Recupera el modo seguro Windows actual. Windows puede estar en modo bloqueado, en modo normal desbloqueado o en modo de prueba.

## <a name="syntax"></a>Sintaxis


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lockdownMode* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, devuelve un MODO DE BLOQUEO DE [**\_ WINDOWS \_ PWLDP \_**](wldp-windows-lockdown-mode.md) que indica el modo seguro para el dispositivo Windows 10 actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ OK si se** realiza correctamente o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




