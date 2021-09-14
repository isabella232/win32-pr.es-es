---
description: Si el Módulo de plataforma segura (TPM) está disponible, este método protege la clave de cifrado del volumen.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Método ProtectKeyWithTPM de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068984"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithTPM de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithTPM** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el hardware de seguridad de Módulo de plataforma segura (TPM) en el equipo, si está disponible.

Se crea un protector de clave de tipo "TPM" para el volumen, si aún no existe uno.

Este método solo es aplicable al volumen que contiene el sistema operativo que se está ejecutando actualmente y si aún no existe un protector de clave en el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se usa un valor en blanco.

</dd> <dt>

*PlatformValidationProfile* \[ en, opcional\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de enteros que especifica cómo el hardware de seguridad Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.

Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos. Se omiten los valores repetidos en el parámetro . Cada índice pcr está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo. Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de la plataforma no han cambiado. Si alguno de estos servicios cambia mientras la protección de Cifrado de unidad BitLocker (BDE) permanece en funcionamiento, el TPM no liberará la clave de cifrado para desbloquear el volumen del disco y el equipo entrará en modo de recuperación.

Si se especifica este parámetro mientras se ha habilitado el directiva de grupo correspondiente, debe coincidir con el directiva de grupo configuración.

Si no se especifica este parámetro, se usa el valor predeterminado de 0, 2, 4, 5, 8, 9, 10 y 11. El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a cambios en la raíz principal de confianza de medida (CRTM), BIOS y extensiones de plataforma (PCR 0), código ROM de opción (PCR 2), código de registro de arranque maestro (MBR) (PCR 4), tabla de particiones del registro de arranque maestro (MBR) (PCR 5), sector de arranque NTFS (PCR 8), código de arranque NTFS (PCR 9),  El Administrador de arranque (PCR 10) y el Cifrado de unidad BitLocker Access Control (PCR 11). Para la seguridad del equipo, se recomienda el perfil predeterminado. Los equipos Extensible Firmware Interface basados en Extensible Firmware Interface (UEFI) no usan PCR 5 de forma predeterminada. Para obtener protección adicional contra los cambios de configuración de inicio temprano, use un perfil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

Cambiar desde el perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo. La sensibilidad de BitLocker a las modificaciones de la plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR. Para habilitar la protección de BitLocker, el perfil de validación de la plataforma debe incluir PCR 11.



| Value                                                                         | Significado                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Raíz principal de confianza de las extensiones de medida (CRTM), BIOS y plataforma.<br/> |
| <dl> <dt>1</dt> </dl>  | Configuración y datos de plataforma y placa base<br/>                          |
| <dl> <dt>2</dt> </dl>  | Código ROM de opción<br/>                                                          |
| <dl> <dt>3</dt> </dl>  | Configuración y datos de ROM de opción<br/>                                        |
| <dl> <dt>4</dt> </dl>  | Código de registro de arranque maestro (MBR)<br/>                                            |
| <dl> <dt>5</dt> </dl>  | Tabla de particiones de registro de arranque maestro (MBR)<br/>                                 |
| <dl> <dt>6</dt> </dl>  | Eventos de transición y reactivación de estado<br/>                                         |
| <dl> <dt>7</dt> </dl>  | Equipo Manufacturer-Specific<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Sector de arranque NTFS<br/>                                                         |
| <dl> <dt>9</dt> </dl>  | Código de arranque NTFS<br/>                                                           |
| <dl> <dt>10</dt> </dl> | Administrador de arranque<br/>                                                             |
| <dl> <dt>11</dt> </dl> | Cifrado de unidad BitLocker Access Control<br/>                                |
| <dl> <dt>12</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                           |
| <dl> <dt>13</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                           |
| <dl> <dt>14</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                           |
| <dl> <dt>15</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                           |
| <dl> <dt>16</dt> </dl> | Se usa para la depuración<br/>                                                       |
| <dl> <dt>17</dt> </dl> | CRTM dinámico<br/>                                                             |
| <dl> <dt>18</dt> </dl> | Plataforma definida<br/>                                                         |
| <dl> <dt>19</dt> </dl> | Usado por el sistema operativo de confianza<br/>                                         |
| <dl> <dt>20</dt> </dl> | Usado por el sistema operativo de confianza<br/>                                         |
| <dl> <dt>21</dt> </dl> | Usado por el sistema operativo de confianza<br/>                                         |
| <dl> <dt>22</dt> </dl> | Usado por el sistema operativo de confianza<br/>                                         |
| <dl> <dt>23</dt> </dl> | Compatibilidad con aplicaciones<br/>                                                      |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica de forma única el protector creado y que se puede usar para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>        | El volumen está bloqueado.<br/>                                                                                                                                                   |
| <dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl> | No se encuentra ningún TPM compatible en este equipo.<br/>                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME 2150694947**</dt> <dt>(0x80310023)</dt> </dl>       | El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Se proporciona el parámetro *PlatformValidationProfile,* pero sus valores no están dentro del intervalo conocido o no coinciden con la configuración directiva de grupo actualmente en vigor.<br/> |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Ya existe un protector de clave de este tipo.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Consideraciones de seguridad

Para la seguridad del equipo, se recomienda el perfil predeterminado. Para obtener protección adicional contra los cambios de configuración de inicio temprano, use un perfil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

Cambiar desde el perfil predeterminado afecta a la seguridad o facilidad de uso del equipo.

## <a name="remarks"></a>Observaciones

Como máximo, puede existir un protector de clave de tipo "TPM" para un volumen en cualquier momento. Si desea cambiar el nombre para mostrar o el perfil de validación de plataforma usado por un protector de clave "TPM" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPM para** crear uno nuevo.

En el caso de los índices de PCR del 0 al 5, las medidas actuales de los registros se usan para proteger la clave de cifrado. En el caso de los valores de PCR del 8 al 11, las medidas usadas son las que se espera que existan en el siguiente ciclo de inicio.

Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen; por ejemplo, cuando el TPM no se puede validar correctamente con el perfil de validación de la plataforma. Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
