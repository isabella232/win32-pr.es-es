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
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="e8c92-106">IMsTscAxEvents:: OnLogonError (método)</span><span class="sxs-lookup"><span data-stu-id="e8c92-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="e8c92-107">Se le llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c92-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8c92-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="e8c92-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8c92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c92-110">*lError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8c92-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c92-111">El código de error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-111">The logon error code.</span></span> <span data-ttu-id="e8c92-112">Esta lista de códigos no es exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="e8c92-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="e8c92-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitraje \_ de \_ \_ Opciones de rugosidad de código** (-5 (0xFFFFFFFB))</span><span class="sxs-lookup"><span data-stu-id="e8c92-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-114">Winlogon muestra el cuadro de diálogo **contención** de la sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="e8c92-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitraje \_ de \_Inicio de \_ sesión de continuación de código** (-2 (0xFFFFFFFE))</span><span class="sxs-lookup"><span data-stu-id="e8c92-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-116">Winlogon continúa con el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="e8c92-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitraje \_ de El código \_ continúa \_ termina** (-3 (0xFFFFFFFD))</span><span class="sxs-lookup"><span data-stu-id="e8c92-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-118">Winlogon está finalizando en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="e8c92-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="e8c92-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitraje \_ de \_ \_ Cuadro de diálogo Code noperm** (-6 (0xFFFFFFFA))</span><span class="sxs-lookup"><span data-stu-id="e8c92-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-120">Winlogon muestra el cuadro de diálogo **sin permisos** .</span><span class="sxs-lookup"><span data-stu-id="e8c92-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="e8c92-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitraje \_ de \_Cuadro de \_ diálogo de código rechazado** (-7 (0xFFFFFFF9))</span><span class="sxs-lookup"><span data-stu-id="e8c92-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-122">Winlogon muestra el cuadro de diálogo **desconectar** .</span><span class="sxs-lookup"><span data-stu-id="e8c92-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="e8c92-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitraje \_ de \_ \_ Opciones** de reconexión de código (-4 (0xFFFFFFFC))</span><span class="sxs-lookup"><span data-stu-id="e8c92-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-124">Winlogon muestra el cuadro de diálogo **volver a conectar** .</span><span class="sxs-lookup"><span data-stu-id="e8c92-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="e8c92-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Error \_ de \_Acceso \_ denegado al código** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="e8c92-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-126">Se denegó el acceso al usuario.</span><span class="sxs-lookup"><span data-stu-id="e8c92-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="e8c92-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Inicio de sesión \_ ERROR \_ de \_ contraseña incorrecta** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="e8c92-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-128">Error de inicio de sesión porque las credenciales de inicio de sesión no son válidas.</span><span class="sxs-lookup"><span data-stu-id="e8c92-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="e8c92-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Inicio de sesión \_ NO \_ superado** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="e8c92-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-130">Se produjo otro error de inicio de sesión o posterior al inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="e8c92-131">El Escritorio remoto cliente muestra una pantalla de inicio de sesión al usuario.</span><span class="sxs-lookup"><span data-stu-id="e8c92-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="e8c92-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Inicio de sesión \_ NO se pudo \_ actualizar la \_ contraseña** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e8c92-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-133">La contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e8c92-133">The password is expired.</span></span> <span data-ttu-id="e8c92-134">El usuario debe actualizar su contraseña para continuar con el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="e8c92-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Inicio de sesión \_ ADVERTENCIA** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="e8c92-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-136">El cliente de Escritorio remoto muestra un cuadro de diálogo que contiene información importante para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e8c92-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="e8c92-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Estado \_ de \_Restricción de cuenta** (-1073741714 (0xC000006E))</span><span class="sxs-lookup"><span data-stu-id="e8c92-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-138">El nombre de usuario y la información de autenticación son válidos, pero la autenticación se bloqueó debido a las restricciones de la cuenta de usuario, como las restricciones de hora del día.</span><span class="sxs-lookup"><span data-stu-id="e8c92-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="e8c92-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Estado \_ de \_Error de inicio de sesión** (-1073741715 (0xC000006D))</span><span class="sxs-lookup"><span data-stu-id="e8c92-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-140">El intento de inicio de sesión no es válido.</span><span class="sxs-lookup"><span data-stu-id="e8c92-140">The attempted logon is not valid.</span></span> <span data-ttu-id="e8c92-141">Esto se debe a un nombre de usuario incorrecto o a la información de autenticación incorrecta.</span><span class="sxs-lookup"><span data-stu-id="e8c92-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="e8c92-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Estado \_ de La contraseña \_ debe \_ cambiar** (-1073741276 (0xC0000224))</span><span class="sxs-lookup"><span data-stu-id="e8c92-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="e8c92-143">La contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e8c92-143">The password is expired.</span></span> <span data-ttu-id="e8c92-144">El usuario debe actualizar su contraseña para continuar con el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c92-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8c92-145">Return value</span></span>

<span data-ttu-id="e8c92-146">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e8c92-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c92-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8c92-147">Remarks</span></span>

<span data-ttu-id="e8c92-148">Implemente este método en el receptor de eventos para recibir una notificación de que se ha producido un error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8c92-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="e8c92-149">Esta lista de códigos no es exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="e8c92-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c92-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c92-150">Requirements</span></span>



| <span data-ttu-id="e8c92-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c92-151">Requirement</span></span> | <span data-ttu-id="e8c92-152">Value</span><span class="sxs-lookup"><span data-stu-id="e8c92-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c92-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8c92-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c92-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8c92-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8c92-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8c92-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c92-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8c92-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8c92-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e8c92-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8c92-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c92-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8c92-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8c92-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8c92-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c92-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8c92-161">IID</span><span class="sxs-lookup"><span data-stu-id="e8c92-161">IID</span></span><br/>                      | <span data-ttu-id="e8c92-162">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e8c92-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e8c92-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8c92-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c92-164">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e8c92-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





