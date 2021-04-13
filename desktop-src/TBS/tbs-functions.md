---
title: Funciones de TBS
description: TBS proporciona las siguientes funciones.
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- Servicios base de TPM TBS, funciones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421080"
---
# <a name="tbs-functions"></a>Funciones de TBS

TBS proporciona las siguientes funciones.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Crear contexto de TBSi \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | Crea un identificador de contexto que se puede usar para pasar comandos a TBS.<br/>                                                                               |
| [**TBSi \_ crear \_ atestación \_ desde el \_ registro**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | Crea una atestación mediante la extracción de un TrustPoint de un registro de TCG.<br/>                                                                                |
| [**TBSi \_ GetDeviceInfo**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | Obtiene la versión del TPM en el equipo.<br/>                                                                                                  |
| [**TBSi \_ obtener \_ OwnerAuth**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | Recupera la autorización de propietario del TPM si la información está disponible en el registro local. <br/>                                             |
| [**TBSi \_ obtener \_ registro de TCG \_**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | Recupera el registro de configuración de arranque de Windows más reciente (WBCL), también denominado registro de TCG.<br/>                                                  |
| [**TBSi \_ obtener \_ registro de TCG \_ \_ ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | Obtiene el registro de configuración de arranque de Windows (WBCL), también denominado registro de TCG, del tipo especificado.<br/>                                          |
| [**TBSi \_ obtener \_ registros de TCG \_**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | Obtiene uno o más registros de configuración de arranque de Windows (WBCL), también denominados registros de TCG.<br/>                                                        |
| [**\_Comando de \_ presencia \_ física de TBSi**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | Pasa un comando ACPI de presencia física a través de TBS al controlador.<br/>                                                                               |
| [**TBSi \_ revocar la \_ atestación**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | Invalida la PCR si el controlador ELAM detecta una infracción de directiva (por ejemplo, un rootkit).<br/>                                                     |
| [**Tbsip \_ Cancelar \_ comandos**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | Cancela todos los comandos pendientes para el contexto especificado.<br/>                                                                                      |
| [**\_Cierre de contexto de Tbsip \_**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | Cierra un identificador de contexto, que libera los recursos asociados al contexto en TBS y cierra el identificador de enlace utilizado para comunicarse con TBS.<br/> |
| [**Tbsip \_ enviar \_ comando**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | Envía un comando de Módulo de plataforma segura (TPM) a los servicios base de TPM (TBS) para su procesamiento.<br/>                                                       |



 

 

