---
description: Si el Módulo de plataforma segura (TPM) está disponible, este método protege la clave de cifrado del volumen mejorada por una clave externa.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Método ProtectKeyWithTPMAndStartupKey de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a15d001f3a92db2e9cb47cd319bbae4ab05ba9bf86b2105f30872159b237718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667135"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithTPMAndStartupKey de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithTPMAndStartupKey** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el hardware de seguridad de Módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por una clave externa que debe presentarse al equipo en el inicio.

Tanto la validación por el TPM como la entrada de un dispositivo de memoria USB que contiene la clave externa son necesarias para acceder a la clave de cifrado del volumen y desbloquear el contenido del volumen. Use el [**método SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para guardar esta clave externa en un archivo en un dispositivo de memoria USB para su uso como clave de inicio.

Este método solo es aplicable al volumen que contiene el sistema operativo que se está ejecutando actualmente.

Se crea un protector de clave de tipo "TPM y clave de inicio" para el volumen, si aún no existe uno.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se usa un valor en blanco.

</dd> <dt>

*PlatformValidationProfile* \[ in, opcional\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de enteros que especifica cómo el hardware de seguridad Módulo de plataforma segura (TPM) del equipo protege la clave de cifrado del volumen de disco.

Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos. Los valores repetidos en el parámetro se omiten. Cada índice de PCR está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo. Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de la plataforma no han cambiado. Si alguno de estos servicios cambia mientras la protección de Cifrado de unidad BitLocker (BDE) permanece en funcionamiento, el TPM no liberará la clave de cifrado para desbloquear el volumen del disco y el equipo entrará en modo de recuperación.

Si se especifica este parámetro mientras se ha habilitado el directiva de grupo de configuración correspondiente, debe coincidir con directiva de grupo configuración.

Si no se especifica este parámetro, se usa el valor predeterminado de 0, 2, 4, 5, 8, 9, 10 y 11. El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a cambios en los siguientes elementos:

-   Raíz principal de la confianza de la medida (CRTM)
-   BIOS
-   Extensiones de plataforma (PCR 0)
-   Código ROM de opción (PCR 2)
-   Código de registro de arranque maestro (MBR) (PCR 4)
-   Tabla de particiones de registro de arranque maestro (MBR) (PCR 5)
-   Sector de arranque de NTFS (PCR 8)
-   Bloque de arranque de NTFS (PCR 9)
-   Administración de arranque (PCR 10)
-   Control de acceso de BitLocker (PCR 11)

Para la seguridad del equipo, se recomienda el perfil predeterminado. Para obtener protección adicional contra los cambios de configuración de inicio temprano, use un perfil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11. Los equipos Extensible Firmware Interface basados en Extensible Firmware Interface (UEFI) no usan PCR 5 de forma predeterminada.

Cambiar del perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo. La confidencialidad de BitLocker con las modificaciones de plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR. Para que la protección de BitLocker esté habilitada, el perfil de validación de la plataforma debe incluir PCR 11.



| Valor                                                                         | Significado                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Raíz principal de confianza de medida (CRTM), BIOS y extensiones de plataforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configuración y datos de plataforma y placa base<br/>                         |
| <dl> <dt>2</dt> </dl>  | Código ROM de opción<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuración y datos de ROM de opción<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Código de registro de arranque maestro (MBR)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabla de particiones de registro de arranque maestro (MBR)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Eventos de transición y reactivación de estado<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Equipo Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Sector de arranque NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloque de arranque NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Administrador de arranque<br/>                                                            |
| <dl> <dt>11</dt> </dl> | BitLocker Access Control<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>13</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>14</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>15</dt> </dl> | Definido para su uso por el sistema operativo estático<br/>                          |
| <dl> <dt>16</dt> </dl> | Se usa para la depuración<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinámico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Plataforma definida<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>23</dt> </dl> | Compatibilidad con aplicaciones<br/>                                                     |



 

</dd> <dt>

*ExternalKey* \[ in, opcional\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits que se usa para desbloquear el volumen cuando se inicia el equipo.

Si no se especifica ninguna clave externa, se genera una aleatoriamente. Use el [**método GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obtener la clave generada aleatoriamente.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que es el identificador único asociado al protector de clave creado que se puede usar para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>        | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                       |
| <dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl> | No se encuentra ningún TPM compatible en este equipo.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.<br/>                                                                                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Se proporciona el parámetro *PlatformValidationProfile,* pero sus valores no están dentro del intervalo conocido o no coinciden con la configuración de directiva de grupo actualmente en vigor.<br/> Se proporciona el parámetro *ExternalKey,* pero no es una matriz de tamaño 32.<br/> |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>       | En este equipo se encuentra un CD/DVD de arranque. Quite el CD/DVD y reinicie el equipo.<br/>                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694961 (0x80310031)</dt> </dl>     | Ya existe un protector de clave de este tipo.<br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Para la seguridad del equipo, se recomienda el perfil predeterminado. Para obtener protección adicional contra los cambios de código de inicio temprano, use un perfil de PCR 0, 2, 4, 5, 8, 9, 10 y 11. Para obtener protección adicional contra los cambios de configuración de inicio temprano, use un perfil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

Cambiar desde el perfil predeterminado afecta a la seguridad o facilidad de uso del equipo.

## <a name="remarks"></a>Comentarios

Como máximo, puede existir un protector de clave de tipo "TPM y clave de inicio" para un volumen en cualquier momento. Si desea cambiar el nombre para mostrar o el perfil de validación de la plataforma que usa un protector de clave "TPM más clave de inicio" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPMAndStartupKey** para crear uno nuevo. Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen; por ejemplo, cuando el TPM no se puede validar correctamente con el perfil de validación de la plataforma o cuando se pierde la memoria USB que contiene la clave externa.

Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.

Aunque es posible tener un protector de clave del tipo "TPM" y otro del tipo "TPM y clave de inicio", la presencia del tipo de protector de clave "TPM" niega los efectos de otros protectores de clave basados en TPM.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
