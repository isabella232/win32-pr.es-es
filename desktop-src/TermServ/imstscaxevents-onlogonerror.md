---
title: Método IMsTscAxEvents OnLogonError
description: Se llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Método OnLogonError Servicios de Escritorio remoto
- Método OnLogonError Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto , método OnLogonError
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
ms.openlocfilehash: 29e2b7e13b4471b476ae00ff4cd810a7955c4e3224744435d37f5a962db834cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125105"
---
# <a name="imstscaxeventsonlogonerror-method"></a>Método IMsTscAxEvents::OnLogonError

Se llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.

## <a name="syntax"></a>Sintaxis


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lError* \[ En\]
</dt> <dd>

Código de error de inicio de sesión. Esta lista de códigos no es exhaustiva.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRAJE \_ OPCIONES \_ DE \_ PROTUBERANCIA** DE CÓDIGO (-5 (0xFFFFFFFB))


</dt> <dd>

Winlogon muestra el cuadro **de diálogo Contención de** sesión.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRAJE \_ CODE \_ CONTINUE \_ LOGON** (-2 (0xFFFFFFFE))


</dt> <dd>

Winlogon continúa con el proceso de inicio de sesión.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRAJE \_ CODE \_ CONTINUE \_ TERMINATE** (-3 (0xFFFFFFFD))


</dt> <dd>

Winlogon termina en modo silencioso.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRAJE \_ CUADRO \_ DE DIÁLOGO CODE NOPERM \_** (-6 (0xFFFFFFFA))


</dt> <dd>

Winlogon muestra el **cuadro de diálogo Sin** permisos.

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRAJE \_ CUADRO \_ DE DIÁLOGO CÓDIGO \_ RECHAZADO** (-7 (0xFFFFFFF9))


</dt> <dd>

Winlogon muestra el cuadro **de diálogo Desconectar** rechazado.

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRAJE \_ OPCIONES \_ DE CODE RECONN \_** (-4 (0xFFFFFFFC))


</dt> <dd>

Winlogon muestra el cuadro de **diálogo Volver** a conectar.

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR \_ ACCESO \_ DE \_ CÓDIGO DENEGADO** (-1 (0xFFFFFFFF))


</dt> <dd>

Se denegó el acceso al usuario.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON \_ CONTRASEÑA \_ INCORRECTA \_ CON ERROR** (0 (0x0))


</dt> <dd>

Error de inicio de sesión porque las credenciales de inicio de sesión no son válidas.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON \_ FAILED \_ OTHER** (2 (0x2))


</dt> <dd>

Se produjo otro error de inicio de sesión o posterior al inicio de sesión. El Escritorio remoto muestra una pantalla de inicio de sesión al usuario.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON \_ CONTRASEÑA \_ DE \_ ACTUALIZACIÓN CON** ERROR (1 (0x1))


</dt> <dd>

La contraseña ha expirado. El usuario debe actualizar su contraseña para seguir iniciando sesión.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON \_ WARNING** (3 (0x3))


</dt> <dd>

El Escritorio remoto muestra un cuadro de diálogo que contiene información importante para el usuario.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**ESTADO \_ RESTRICCIÓN \_ DE** CUENTA (-1073741714 (0xC000006E))


</dt> <dd>

El nombre de usuario y la información de autenticación son válidos, pero la autenticación se bloqueó debido a restricciones en la cuenta de usuario, como restricciones de hora del día.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**ESTADO \_ ERROR \_ DE INICIO** DE SESIÓN (-1073741715 (0xC000006D))


</dt> <dd>

El intento de inicio de sesión no es válido. Esto se debe a un nombre de usuario incorrecto o a una información de autenticación incorrecta.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**ESTADO \_ PASSWORD \_ MUST \_ CHANGE** (-1073741276 (0xC0000224))


</dt> <dd>

La contraseña ha expirado. El usuario debe actualizar su contraseña para seguir iniciando sesión.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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

 

 





