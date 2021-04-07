---
description: Indica si el TPM está listo y proporciona información adicional sobre el estado del TPM.
ms.assetid: 1E348D77-979C-42FC-824D-7C57F7BAABE5
title: 'Win32_Tpm:: IsReadyInformation (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReadyInformation
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 23f3b2f38ea12bac19230f1871d30c84098eb1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002664"
---
# <a name="win32_tpmisreadyinformation-method"></a>Win32 \_ TPM:: IsReadyInformation (método)

Indica si el TPM está listo y proporciona información adicional sobre el estado del TPM. El parámetro de información devuelve una máscara de la información de lo que se necesita para aprovisionar completamente el TPM.

Este método solo es accesible para los administradores locales.

## <a name="syntax"></a>Sintaxis


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsReady* \[ enuncia\]
</dt> <dd>

Establézcalo en **true** si el TPM y el sistema están totalmente aprovisionados para el uso de TPM.

</dd> <dt>

*Información* \[ de enuncia\]
</dt> <dd>

Devuelve una máscara de la cantidad de información disponible de lo que se necesita para aprovisionar completamente el TPM.

El parámetro de *información* puede constar de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**Información \_ de SHUTDOWN**</dt> <dt>0x00000002</dt> </dl>                                                 | Es necesario reiniciar la plataforma (apagado).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**Información \_ de REINICIAR**</dt> <dt>0x00000004</dt> </dl>                                                       | Es necesario reiniciar la plataforma (reinicio).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**Información \_ de \_Forzar \_ desactivación de TPM**</dt> <dt></dt> </dl>                          | El TPM ya es propiedad. Es necesario borrar TPM o se debe importar el valor de autorización de propietario de TPM.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**Información \_ de \_Presencia física**</dt> <dt>0x00000010</dt> </dl>                     | La presencia física es necesaria para aprovisionar el TPM.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**Información \_ de \_Activación de TPM**</dt> <dt>0x00000020</dt> </dl>                                    | El TPM está deshabilitado o desactivado.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**Información \_ de \_Tomar \_ posesión**</dt> de <dt>0x00000040</dt> de TPM </dl>                 | Se tomó la propiedad del TPM.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**Información \_ de TPM \_ Create \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Existe una clave de aprobación (EK) en el TPM. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**Información \_ de 0x00000100 \_ OWNERAUTH TPM**</dt> <dt></dt> </dl>                                 | La autorización de propietario del TPM no está correctamente almacenada en el registro.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Información \_ de 0x00000200 \_ de \_ autenticación SRK de TPM**</dt> <dt></dt> </dl>                                  | El valor de autorización de la clave raíz de almacenamiento (SRK) no es todo ceros.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Información \_ de TPM \_ deshabilitar \_ propietario \_**</dt> desactivado <dt>0x00000400</dt> </dl> | Si el sistema operativo está configurado para deshabilitar el borrado del TPM con el valor de autorización de propietario de TPM y el TPM aún no se ha configurado para impedir que el TPM se desactive con el valor de autorización de propietario del TPM.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Información \_ de 0x00000800 \_ SRKPUB TPM**</dt> <dt></dt> </dl>                                          | La información del registro del sistema operativo acerca de la clave raíz de almacenamiento del TPM no coincide con la clave raíz de almacenamiento del TPM.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Información \_ de \_Lectura de \_ SRKPUB**</dt> <dt>0x00001000</dt> de TPM </dl>                          | No se ha establecido la marca permanente del TPM para permitir la lectura del valor público de la clave raíz de almacenamiento.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Información \_ de \_ \_ Contador de arranque de TPM**</dt> <dt>0x00002000</dt> </dl>                       | El contador monotónico incrementado durante el arranque no se ha creado.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Información \_ de 0x00004000 \_ de \_ copia de seguridad de ad de TPM**</dt> <dt></dt> </dl>                                | No se ha realizado una copia de seguridad de la autorización del propietario del TPM en Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Información \_ de \_Fase de \_ copia \_ \_ de seguridad de ad de TPM**</dt> <dt>0x00008000</dt> </dl>      | La primera parte del almacenamiento de información de autorización de propietario de TPM en Active Directory está en curso.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Información \_ de \_ \_ \_ Fase \_ II**</dt> <dt>0x00010000</dt> de copia de seguridad de ad de TPM </dl>   | La segunda parte del almacenamiento de información de autorización de propietario de TPM en Active Directory está en curso.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Información \_ de \_Configuración heredada**</dt> <dt>0x00020000</dt> </dl>            | Windows directiva de grupo está configurado para no almacenar ninguna autorización de propietario de TPM, por lo que el TPM no puede estar totalmente preparado.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Información \_ de \_Certificado EK**</dt> <dt>0x00040000</dt> </dl>                              | El certificado EK no se leyó de la RAM NV de TPM y se almacenó en el registro. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Información \_ de \_ \_ Registro de eventos de TCG**</dt> <dt>0x00080000</dt> </dl>                                | El registro de eventos de TCG está vacío o no se puede leer. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Información \_ de 0x00100000 no \_ reducido**</dt> <dt></dt> </dl>                                       | El TPM no es propiedad.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Información \_ de \_Error genérico**</dt> <dt>0x00200000</dt> </dl>                                 | Se produjo un error, pero no es específico de una tarea determinada.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Información \_ de \_ \_ Contador de bloqueo de dispositivo**</dt> <dt>0x00400000</dt> </dl>              | No se ha creado el contador de bloqueo del dispositivo.<br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <dt>**Información \_ de DEVICEID**</dt> <dt> 0x00800000</dt> </dl>                                                | No se ha creado el identificador de dispositivo.<br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <dt>**Información \_ de \_Vulnerabilidad de atestación**</dt> <dt> 0x01000000</dt> </dl>                                                | El TPM tiene una vulnerabilidad relacionada con la atestación de estado.<br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
