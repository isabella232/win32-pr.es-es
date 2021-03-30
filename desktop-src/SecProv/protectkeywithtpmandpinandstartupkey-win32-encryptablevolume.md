---
description: Protege la clave de cifrado del volumen mediante el Módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por un número de identificación personal (PIN) especificado por el usuario y por una clave externa que se debe presentar al equipo en el inicio.
ms.assetid: 8991c22c-1e36-415e-a82b-c5ddf9c3b24a
title: Método ProtectKeyWithTPMAndPINAndStartupKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPINAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9f315629c810027e18dac3a337c126f4a4a4bcce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815723"
---
# <a name="protectkeywithtpmandpinandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithTPMAndPINAndStartupKey de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithTPMAndPINAndStartupKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por un número de identificación personal (PIN) especificado por el usuario y por una clave externa que se debe presentar al equipo en el inicio.

Se necesitan tres factores de autenticación para desbloquear el contenido cifrado del volumen:

1.  Validación por parte del TPM
2.  Entrada de un PIN de 4 a 20 dígitos o, si la Directiva de grupo "permitir PIN mejorados para el inicio" está habilitada, de 4 a 20 letras, símbolos, espacios o números
3.  Entrada de un dispositivo de memoria USB que contiene la clave externa

Use el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para guardar esta clave externa en un archivo en un dispositivo de memoria USB para su uso como clave de inicio. Este método solo se aplica en el volumen del sistema operativo. Se crea un protector de clave de tipo "TPM y PIN y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithTPMAndPINAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile,
  [in]           string PIN,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que etiqueta este protector de clave. Si no se especifica este parámetro, se utiliza un valor en blanco.

</dd> <dt>

*PlatformValidationProfile* \[ en, opcional\]
</dt> <dd>

Tipo: **Uint8**

Matriz de enteros que especifica cómo el TPM del equipo protege la clave de cifrado del volumen. Un perfil de validación de plataforma consta de un conjunto de índices de registro de configuración de plataforma (PCR) que van de 0 a 23, ambos incluidos. Los valores de repetición del parámetro se omiten. Cada índice de PCR está asociado a los servicios que se ejecutan cuando se inicia el sistema operativo. Cada vez que se inicia el equipo, el TPM comprobará que los servicios especificados en el perfil de validación de plataforma no han cambiado. Si alguno de estos servicios cambia mientras la protección de BitLocker permanece activada, el TPM no liberará la clave de cifrado para desbloquear el volumen y el equipo entrará en modo de recuperación.

Si no se especifica este parámetro, se usan los índices predeterminados de 0, 2, 4, 5, 8, 9, 10 y 11. El perfil de validación de plataforma predeterminado protege la clave de cifrado frente a los cambios en la raíz principal de la confianza de medición (CRTM). BIOS, y extensiones de plataforma (PCR 0), código ROM de opción (PCR 2), código de registro de arranque maestro (MBR) (PCR 4), tabla de particiones de registro de arranque maestro (PCR 5), el sector de arranque de NTFS (PCR 8), el bloque de arranque de NTFS (PCR 9), el administrador de arranque (PCR 10) y el Access Control de BitLocker (PCR 11). De forma predeterminada, los equipos basados en Unified Extensible Firmware Interface (UEFI) no usan PCR 5.

Se recomienda el perfil de validación de plataforma predeterminado. Para obtener protección adicional frente a los cambios de configuración de inicio temprano, use un perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

Cambiar el perfil predeterminado afecta a la seguridad y la capacidad de administración del equipo. La confidencialidad de las modificaciones de BitLocker a plataforma (malintencionadas o autorizadas) aumenta o disminuye en función de la inclusión o exclusión, respectivamente, de las PCR. Para habilitar la protección de BitLocker, el perfil de validación de plataforma debe incluir PCR 11.



| Value                                                                         | Significado                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Raíz principal de la confianza de medición (CRTM), BIOS y extensiones de plataforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configuración y datos de la plataforma y la placa base<br/>                         |
| <dl> <dt>2</dt> </dl>  | Código ROM de opción<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuración y datos de ROM de opción<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Código de registro de arranque maestro (MBR)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabla de partición de registro de arranque maestro (MBR)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Transición de estado y eventos de activación<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Manufacturer-Specific de equipo<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Sector de arranque de NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloque de arranque de NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Administrador de arranque<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Access Control de BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definido para que lo use el sistema operativo estático<br/>                          |
| <dl> <dt>13</dt> </dl> | Definido para que lo use el sistema operativo estático<br/>                          |
| <dl> <dt>14</dt> </dl> | Definido para que lo use el sistema operativo estático<br/>                          |
| <dl> <dt>15</dt> </dl> | Definido para que lo use el sistema operativo estático<br/>                          |
| <dl> <dt>16</dt> </dl> | Se usa para la depuración<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinámico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Plataforma definida<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usado por un sistema operativo de confianza<br/>                                      |
| <dl> <dt>23</dt> </dl> | Compatibilidad con aplicaciones<br/>                                                     |



 

</dd> <dt>

*Código PIN* \[ de\]
</dt> <dd>

Tipo: **String**

Contiene un número de identificación personal (PIN) de 4 a 20 dígitos o, si la Directiva de grupo "permitir PIN mejorados para el inicio" está habilitada, 4 y 20 letras, símbolos, espacios o números. Esta cadena se debe proporcionar al equipo en el inicio.

</dd> <dt>

*ExternalKey* \[ en, opcional\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen cuando se inicia el equipo. Deje este parámetro en blanco para generar de forma aleatoria la clave externa. Use el método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obtener la clave generada de forma aleatoria.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                | Método realizado correctamente.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Se proporciona el parámetro *PlatformValidationProfile* , pero sus valores no están dentro del intervalo conocido o no coinciden con el valor Directiva de grupo que está actualmente en vigor.<br/> Se proporciona el parámetro *ExternalKey* , pero no es una matriz de tamaño 32.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | En este equipo se encuentra un CD/DVD de arranque. Quite el CD o el DVD y reinicie el equipo.<br/>                                                                                                                                                                               |
| <dl> <dt>**FVE \_ \_ \_ Volumen externo E**</dt> <dt>2150694947 (0x80310023)</dt> </dl>              | El TPM no puede proteger la clave de cifrado del volumen porque el volumen no contiene el sistema operativo que se está ejecutando actualmente.<br/>                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ \_ \_ caracteres de PIN no válidos**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | El parámetro *NewPIN* contiene caracteres que no son válidos. Cuando el directiva de grupo "permitir PIN mejorados para el inicio" está deshabilitado, solo se admiten los números.<br/>                                                                                                        |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ \_Longitud de \_ \_ PIN no \_ válida de la Directiva E**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | El parámetro *NewPIN* proporcionado tiene más de 20 caracteres, menos de 4 caracteres, o menor que la longitud mínima especificada por directiva de grupo.<br/>                                                                                                          |
| <dl> <dt>**FVE \_ El \_ protector E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Ya existe un protector de clave de este tipo.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | No se encuentra ningún TPM compatible en este equipo.<br/>                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

Como máximo, puede existir un protector de clave de tipo "TPM y PIN y clave de inicio" para un volumen en cualquier momento. Si desea cambiar el nombre para mostrar o el perfil de validación de plataforma usado por un protector de clave "TPM y PIN y clave de inicio" existente, primero debe quitar el protector de clave existente y, a continuación, llamar a **ProtectKeyWithTPMAndPINAndStartupKey** para crear uno nuevo.

Se deben especificar protectores de clave adicionales para desbloquear el volumen en escenarios de recuperación en los que no se puede obtener acceso a la clave de cifrado del volumen. por ejemplo, cuando el TPM no se puede validar correctamente con el perfil de validación de plataforma o cuando se pierde el PIN. Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para crear uno o varios protectores de clave para recuperar un volumen bloqueado de otro modo.

Aunque es posible tener tanto un protector de clave del tipo "TPM" como otro del tipo "TPM y el PIN y la clave de inicio", la presencia del tipo de protector de clave "TPM" niega los efectos de otros protectores de clave basados en TPM.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise con SP1, Windows Vista Ultimate con SP1 \[ solo aplicaciones de escritorio\]<br/>     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
