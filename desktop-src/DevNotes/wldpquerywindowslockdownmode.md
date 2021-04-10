---
description: Recupera el modo seguro de Windows actual. Windows puede estar en modo bloqueado, modo normal desbloqueado o modo de prueba.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Función WldpQueryWindowsLockdownMode (WLDP. h)
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
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275048"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode función)

Recupera el modo seguro de Windows actual. Windows puede estar en modo bloqueado, modo normal desbloqueado o modo de prueba.

## <a name="syntax"></a>Sintaxis


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lockdownMode* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve un [**\_ modo de \_ bloqueo \_ de Windows PWLDP**](wldp-windows-lockdown-mode.md) que indica el modo seguro para el dispositivo de Windows 10 actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




