---
description: Describe los modos seguros (modos S) de un Windows dispositivo.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE enumeración (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911345"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>Enumeración WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE

Describe los modos seguros (modos S) de un Windows dispositivo. Se usa principalmente en [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**MODO DE BLOQUEO DE WINDOWS DE WLDP \_ \_ \_ \_ DESBLOQUEADO**
</dt> <dd>

Desbloqueado. Se usa principalmente para Windows dispositivos sin el modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**PRUEBA DEL MODO \_ DE BLOQUEO DE WINDOWS \_ \_ DE \_ WLDP**
</dt> <dd>

Juicio. Se usa principalmente para un Windows 10 de prueba con el modo S. El modo de prueba es un caso especial para Windows 10 dispositivos con el modo S: se aplican directivas, pero no hay ninguna protección contra la reversión para la aplicación de la directiva.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**MODO DE BLOQUEO DE WINDOWS DE WLDP \_ \_ \_ \_ BLOQUEADO**
</dt> <dd>

Bloqueado. Se usa principalmente para un Windows 10 con el modo S. Un dispositivo bloqueado aplicará las directivas de Device Guard firmadas que se envían con la Windows 10 del sistema operativo con el modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**MODO DE BLOQUEO DE WINDOWS DE WLDP \_ \_ \_ \_ MÁX.**
</dt> <dd>

Valor máximo de enumeración.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wldp.h</dt> </dl> |



 

 




