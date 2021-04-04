---
title: IMsTscAxEvents OnLogonError, método
description: Se le llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Método OnLogonError Servicios de Escritorio remoto
- Método OnLogonError Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802738"
---
# <a name="imstscaxeventsonlogonerror-method"></a>IMsTscAxEvents:: OnLogonError (método)

Se le llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.

## <a name="syntax"></a>Sintaxis


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lError* \[ de\]
</dt> <dd>

El código de error de inicio de sesión. Esta lista de códigos no es exhaustiva.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitraje \_ de \_ \_ Opciones de rugosidad de código** (-5 (0xFFFFFFFB))


</dt> <dd>

Winlogon muestra el cuadro de diálogo **contención** de la sesión.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitraje \_ de \_Inicio de \_ sesión de continuación de código** (-2 (0xFFFFFFFE))


</dt> <dd>

Winlogon continúa con el proceso de inicio de sesión.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitraje \_ de El código \_ continúa \_ termina** (-3 (0xFFFFFFFD))


</dt> <dd>

Winlogon está finalizando en modo silencioso.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitraje \_ de \_ \_ Cuadro de diálogo Code noperm** (-6 (0xFFFFFFFA))


</dt> <dd>

Winlogon muestra el cuadro de diálogo **sin permisos** .

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitraje \_ de \_Cuadro de \_ diálogo de código rechazado** (-7 (0xFFFFFFF9))


</dt> <dd>

Winlogon muestra el cuadro de diálogo **desconectar** .

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitraje \_ de \_ \_ Opciones** de reconexión de código (-4 (0xFFFFFFFC))


</dt> <dd>

Winlogon muestra el cuadro de diálogo **volver a conectar** .

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Error \_ de \_Acceso \_ denegado al código** (-1 (0xFFFFFFFF))


</dt> <dd>

Se denegó el acceso al usuario.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Inicio de sesión \_ ERROR \_ de \_ contraseña incorrecta** (0 (0X0))


</dt> <dd>

Error de inicio de sesión porque las credenciales de inicio de sesión no son válidas.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Inicio de sesión \_ NO \_ superado** (2 (0X2))


</dt> <dd>

Se produjo otro error de inicio de sesión o posterior al inicio de sesión. El Escritorio remoto cliente muestra una pantalla de inicio de sesión al usuario.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Inicio de sesión \_ NO se pudo \_ actualizar la \_ contraseña** (1 (0x1))


</dt> <dd>

La contraseña ha expirado. El usuario debe actualizar su contraseña para continuar con el inicio de sesión.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Inicio de sesión \_ ADVERTENCIA** (3 (0X3))


</dt> <dd>

El cliente de Escritorio remoto muestra un cuadro de diálogo que contiene información importante para el usuario.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Estado \_ de \_Restricción de cuenta** (-1073741714 (0xC000006E))


</dt> <dd>

El nombre de usuario y la información de autenticación son válidos, pero la autenticación se bloqueó debido a las restricciones de la cuenta de usuario, como las restricciones de hora del día.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Estado \_ de \_Error de inicio de sesión** (-1073741715 (0xC000006D))


</dt> <dd>

El intento de inicio de sesión no es válido. Esto se debe a un nombre de usuario incorrecto o a la información de autenticación incorrecta.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Estado \_ de La contraseña \_ debe \_ cambiar** (-1073741276 (0xC0000224))


</dt> <dd>

La contraseña ha expirado. El usuario debe actualizar su contraseña para continuar con el inicio de sesión.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Implemente este método en el receptor de eventos para recibir una notificación de que se ha producido un error de inicio de sesión.

Esta lista de códigos no es exhaustiva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





