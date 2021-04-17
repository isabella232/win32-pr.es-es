---
description: Describe los modos seguros (modos S) de un dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumeración WLDP_WINDOWS_LOCKDOWN_MODE (WLDP. h)
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661214"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>WLDP \_ \_ enumeración del modo de bloqueo de Windows \_

Describe los modos seguros (modos S) de un dispositivo Windows. Se usa principalmente en [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

## <a name="syntax"></a>Sintaxis


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

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modo de bloqueo de Windows WLDP \_ \_ \_ desbloqueado**
</dt> <dd>

Desbloquear. Se usa principalmente para dispositivos Windows sin el modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ \_ prueba de \_ modo de bloqueo de Windows \_**
</dt> <dd>

Periodo. Se usa principalmente para un dispositivo de prueba de Windows 10 con el modo S. El modo de prueba es un caso especial para dispositivos Windows 10 con el modo S: se aplican las directivas, pero no hay protección contra reversión para la aplicación de la Directiva.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ modo de bloqueo de Windows \_ \_ \_ bloqueado**
</dt> <dd>

Cerrado. Se usa principalmente para un dispositivo de Windows 10 con el modo S. Un dispositivo que está bloqueado aplicará las directivas de Device Guard firmadas que se incluyen con la imagen del sistema operativo Windows 10 con el modo S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ modo de bloqueo de Windows \_ \_ \_ máximo**
</dt> <dd>

Valor de enumeración máximo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WLDP. h</dt> </dl> |



 

 




