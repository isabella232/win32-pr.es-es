---
title: Funciones de TBS
description: TBS proporciona las siguientes funciones.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- TPM Base Services TBS , funciones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243782"
---
# <a name="tbs-functions"></a>Funciones de TBS

TBS proporciona las siguientes funciones.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creación de contexto de Tbsi \_ \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Crea un identificador de contexto que se puede usar para pasar comandos a TBS.<br/>                                                                               |
| [**Tbsi \_ Create \_ Attestation \_ From \_ Log**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Crea una atestación mediante la extracción de un TrustPoint de un registro TCG.<br/>                                                                                |
| [**Tbsi \_ GetDeviceInfo**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Obtiene la versión del TPM en el equipo.<br/>                                                                                                  |
| [**Tbsi \_ Get \_ OwnerAuth**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Recupera la autorización del propietario del TPM si la información está disponible en el registro local. <br/>                                             |
| [**Tbsi \_ Get \_ TCG \_ Log**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | Recupera el registro de configuración de Windows de arranque (WBCL) más reciente, también denominado registro TCG.<br/>                                                  |
| [**Tbsi \_ Get \_ TCG \_ Log \_ Ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | Obtiene el Windows de configuración de arranque (WBCL), también denominado registro TCG, del tipo especificado.<br/>                                          |
| [**Tbsi \_ Get \_ TCG \_ Logs**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | Obtenga uno o varios Windows de configuración de arranque (WBCL), también denominados registros de TCG.<br/>                                                        |
| [**Tbsi \_ Physical \_ Presence (Comando de presencia física de \_ Tbsi)**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Pasa un comando ACPI de presencia física a través de TBS al controlador.<br/>                                                                               |
| [**Tbsi \_ Revoke \_ Attestation**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Invalida las PCR si el controlador ELAM detecta una infracción de directiva (por ejemplo, un rootkit).<br/>                                                     |
| [**Tbsip \_ Cancel \_ (Comandos)**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Cancela todos los comandos pendientes para el contexto especificado.<br/>                                                                                      |
| [**Tbsip \_ Context \_ Close**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Cierra un identificador de contexto, que libera los recursos asociados al contexto en TBS y cierra el identificador de enlace utilizado para comunicarse con TBS.<br/> |
| [**Tbsip \_ Submit \_ (Comando)**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Envía un comando Módulo de plataforma segura (TPM) a los Servicios base de TPM (TBS) para su procesamiento.<br/>                                                       |



 

 

