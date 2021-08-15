---
description: Intenta aprovisionar el TPM en un estado completamente listo y asumirá la propiedad de TPM si aún no es propiedad de .
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm::P rovision (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5153672d91c88597676f65b53a93de6ffac9f4989dd9e231c87a3b7947b1d657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890813"
---
# <a name="win32_tpmprovision-method"></a>Método \_ Tpm::P rovision de Win32

Intenta aprovisionar el TPM en un estado completamente listo y asumirá la propiedad de TPM si aún no es propiedad de . Este método es costoso de ejecutar porque realiza muchas comprobaciones. Se recomienda que las aplicaciones utilicen este método solo cuando sea necesario.

Los administradores locales solo pueden acceder a este método.

## <a name="syntax"></a>Sintaxis


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ForceClear \_ Permitido* \[ en\]
</dt> <dd>

Cuando se establece en **TRUE,** el método puede solicitar operaciones de presencia física para borrar el TPM. Si se establece **en FALSE,** el método no solicitará una operación de presencia física para borrar el TPM.

</dd> <dt>

*PhysicalPresencePrompts \_ Permitido* \[ en\]
</dt> <dd>

Cuando se establece en **TRUE,** el método puede solicitar operaciones de presencia física que requieran la intervención del usuario durante el proceso de arranque para confirmar el cambio de estado del TPM.

</dd> <dt>

*Información* \[ out\]
</dt> <dd>

Devuelve una máscara de bits de tanta información como esté disponible de lo que se necesita para aprovisionar completamente el TPM. Los valores de máscara como INFORMATION REBOOT indican que la llamada al método debe iniciar un \_ reinicio para mover el proceso de aprovisionamiento hacia delante.

El *parámetro Information* puede constar de los siguientes valores.



| Valor                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**INFORMACIÓN \_ Apagado**</dt> <dt>0x00000002</dt> </dl>                                                 | Se requiere el reinicio de la plataforma (apagado).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**INFORMACIÓN \_ Reinicio**</dt> <dt>0x00000004</dt> </dl>                                                       | Se requiere el reinicio de la plataforma (reinicio).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ FORCE \_ CLEAR**</dt> <dt>0x00000008</dt> </dl>                          | El TPM ya es propiedad de . Es necesario borrar el TPM o importar el valor de autorización del propietario del TPM.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**INFORMACIÓN \_ PRESENCIA \_ FÍSICA**</dt> <dt>0x00000010</dt> </dl>                     | Se requiere presencia física para aprovisionar el TPM.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ ACTIVATE**</dt> <dt>0x00000020</dt> </dl>                                    | El TPM está deshabilitado o desactivado.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ TOMA \_ POSESIÓN**</dt> <dt>0X00000040</dt> </dl>                 | Se tomó la propiedad de TPM.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ CREATE \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Existe una clave de aprobación (EK) en el TPM. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**INFORMACIÓN \_ Tpm \_ OWNERAUTH**</dt> <dt>0x00000100</dt> </dl>                                 | La autorización del propietario del TPM no se almacena correctamente en el registro.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**INFORMACIÓN \_ Autenticación \_ de TPM \_ SRK**</dt> <dt>0x000000200</dt> </dl>                                  | El Storage de autorización de clave raíz (SRK) no es todos ceros.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ DISABLE OWNER CLEAR \_ \_ 0x00000400**</dt> <dt></dt> </dl> | Si el sistema operativo está configurado para deshabilitar la desactivación del TPM con el valor de autorización del propietario del TPM y el TPM aún no se ha configurado para evitar la eliminación del TPM con el valor de autorización del propietario del TPM .<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**INFORMACIÓN \_ Tpm \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | La información del Registro del sistema operativo sobre la clave raíz Storage del TPM no coincide con la clave raíz Storage TPM.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | La marca permanente de TPM para permitir la lectura del Storage valor público de clave raíz no está establecido.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**INFORMACIÓN \_ Contador \_ de \_ ARRANQUE de TPM**</dt> <dt>0x00002000</dt> </dl>                       | No se ha creado el contador monotónico incrementado durante el arranque.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**INFORMACIÓN \_ Copia de seguridad de AD \_ \_ de TPM**</dt> <dt>0x00004000</dt> </dl>                                | No se ha realizado una copia de seguridad de la autorización del propietario del TPM Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**INFORMACIÓN \_ FASE I DE COPIA DE SEGURIDAD DE TPM \_ AD \_ \_ \_ 0x00008000**</dt> <dt></dt> </dl>      | La primera parte del almacenamiento de información de autorización del propietario del TPM Active Directory está en curso.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**INFORMACIÓN \_ TPM \_ AD BACKUP PHASE II \_ \_ \_ 0x00010000**</dt> <dt></dt> </dl>   | La segunda parte del almacenamiento de información de autorización del propietario del TPM Active Directory está en curso.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**INFORMACIÓN \_ Configuración \_ heredada**</dt> <dt>0x00020000</dt> </dl>            | Windows directiva de grupo está configurado para no almacenar ninguna autorización de propietario de TPM, por lo que el TPM no puede estar totalmente listo.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**INFORMACIÓN \_ Certificado \_ de EK**</dt> <dt>0x00040000</dt> </dl>                              | El certificado EK no se leyó de la ram de NV de TPM y se almacena en el registro. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**INFORMACIÓN \_ Registro de \_ EVENTOS \_ TCG**</dt> <dt>0x00080000</dt> </dl>                                | El registro de eventos TCG está vacío o no se puede leer. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**INFORMACIÓN \_ NOT \_ REDUCED**</dt> <dt>0x00100000</dt> </dl>                                       | El TPM no es propiedad de .<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**INFORMACIÓN \_ ERROR \_ GENÉRICO**</dt> <dt>0x00200000</dt> </dl>                                 | Se produjo un error, pero no es específico de una tarea determinada.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**INFORMACIÓN \_ CONTADOR \_ DE \_ BLOQUEO DE**</dt> DISPOSITIVO <dt>0x00400000</dt> </dl>              | No se ha creado el contador de bloqueo del dispositivo.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de [TPM.](../tbs/tbs-return-codes.md)

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
