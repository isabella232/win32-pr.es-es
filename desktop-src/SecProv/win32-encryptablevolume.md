---
description: Para el cifrado de unidades o para crear software de seguridad de cifrado, puede usar el software de cifrado de Windows, Cifrado de unidad BitLocker, una API de cifrado que puede usar mediante la clase de proveedor \_ WMI EncryptableVolume de Win32.
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3beb3498cf9e3d2873ea7dcfe3a108618eeddb513bc8207d1e819cce2fe976d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891008"
---
# <a name="win32_encryptablevolume-class"></a>Clase \_ EncryptableVolume de Win32

La clase de proveedor WMI **\_ EncryptableVolume de Win32** representa un área de almacenamiento en un disco duro que se puede proteger mediante Cifrado de unidad BitLocker. Solo se pueden cifrar volúmenes NTFS. Puede ser un volumen que contiene un sistema operativo o puede ser un volumen de datos en el disco local. No puede ser una unidad de red.

Para obtener las ventajas de BitLocker, debe especificar un método de protección para la clave de cifrado del volumen y, a continuación, cifrar completamente el volumen.

Para proteger la clave de cifrado del volumen, agregue protectores de clave mediante estos métodos:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Cada tipo de protector de clave proporciona una experiencia de autenticación diferente para desbloquear el acceso a los datos cifrados. Las claves externas y las contraseñas numéricas pueden proporcionar autenticación durante escenarios de recuperación. En el caso de los protectores de claves basados en TPM, es posible que primero tenga que inicializar correctamente el TPM. Para obtener más información, vea la clase [**de proveedor WMI de \_ Tpm win32.**](win32-tpm.md)

Use el [**método Encrypt**](encrypt-win32-encryptablevolume.md) o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) para iniciar el cifrado. Los protectores de clave deben agregarse antes de iniciar el cifrado o, de lo contrario, debe usar el método [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) para exponer una clave sin protección. Si el equipo se apaga mientras el cifrado está en curso, el cifrado se reanudará automáticamente cuando se reinicie el equipo.

Puede usar los [**métodos GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) y [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) para comprobar el estado de un volumen accesible.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>Miembros

La **clase \_ EncryptableVolume de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ EncryptableVolume de Win32** tiene estos métodos.



| Método                                                                                                                   | Descripción                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Guarda todas las claves externas y la información relacionada necesaria para la recuperación en el Active Directory.<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Cambia la clave externa asociada a un volumen cifrado.<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Usa la nueva frase de contraseña para obtener una nueva clave derivada.<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | Cambia un PIN asociado a un volumen cifrado.<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Quita todas las claves externas y la información relacionada guardada en el volumen del sistema operativo que se está ejecutando actualmente y que se usa para desbloquear automáticamente los volúmenes de datos.<br/>                                                                                                             |
| [**Descifrar**](decrypt-win32-encryptablevolume.md)                                                                       | Comienza el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Elimina un protector de clave determinado para el volumen.<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Elimina todos los protectores de clave para el volumen.<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando actualmente para que el volumen no se desbloquee automáticamente cuando se monte.<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Deshabilita todos los protectores de clave asociados a este volumen.<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Permite desbloquear automáticamente un volumen de datos cuando se monta el volumen.<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Habilita todos los protectores de clave deshabilitados.<br/>                                                                                                                                                                                                                                       |
| [**Encrypt**](encrypt-win32-encryptablevolume.md)                                                                       | Comienza el cifrado de un volumen completamente descifrado o reanuda el cifrado de un volumen parcialmente cifrado.<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Comienza el cifrado de un volumen completamente descifrado después de una prueba de hardware.<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | Enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales.<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Indica el estado del cifrado o descifrado en el volumen.<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Indica el algoritmo de cifrado y el tamaño de clave usados en el volumen.<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Devuelve el nombre del archivo que contiene la clave externa.<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Devuelve la clave externa de un archivo.<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Devuelve información de estado en una prueba de hardware.<br/>                                                                                                                                                                                                                             |
| [**GetIdentificationField**](getidentificationfield-win32-encryptablevolume.md)                                         | Devuelve la cadena de identificador que está disponible en los metadatos del volumen.<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Devuelve información que ayuda a recuperar los datos cifrados cuando la unidad está gravemente dañada.<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Recupera la clave pública y la huella digital del certificado para un protector de clave pública.<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Recupera la clave externa para un protector de clave determinado del tipo adecuado.<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Recupera el nombre para mostrar usado para identificar un protector de clave determinado.<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Recupera la contraseña numérica para un protector de clave determinado del tipo adecuado.<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Recupera el perfil de validación de plataforma para un protector de clave determinado del tipo adecuado.<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Enumera los protectores usados para proteger la clave de cifrado del volumen.<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Indica el tipo de un protector de clave determinado.<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Indica si el contenido del volumen es accesible desde el sistema operativo que se está ejecutando actualmente.<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Indica si el volumen y su clave de cifrado (si existe) están protegidos.<br/>                                                                                                                                                                                                  |
| [**GetVersion**](getversion-win32-encryptablevolume.md)                                                                 | Indica la versión de metadatos de FVE del volumen.<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | Indica si el volumen se desbloquea automáticamente cuando se monta.<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Indica si existe en el volumen del sistema operativo que se está ejecutando actualmente cualquier clave externa e información relacionada que se pueda usar para desbloquear automáticamente los volúmenes de datos.<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Indica si hay protectores disponibles para el volumen.<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Indica si la contraseña numérica cumple los requisitos de formato especiales.<br/>                                                                                                                                                                                            |
| [**Lock**](lock-win32-encryptablevolume.md)                                                                             | Desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema.<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Pausa el cifrado o descifrado de un volumen.<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | Crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección.<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Valida el identificador de objeto (OID) uso mejorado de clave (EKU) del archivo de certificado proporcionado.<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Valida el identificador de objeto (OID) uso mejorado de clave (EKU) de la huella digital del certificado proporcionado.<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Protege la clave de cifrado del volumen con una clave externa de 256 bits.<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial.<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Usa la frase de contraseña para obtener la clave derivada.<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Protege la clave de cifrado del volumen mediante el hardware de seguridad Módulo de plataforma segura (TPM) del equipo, si está disponible.<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Protege la clave de cifrado del volumen mediante el hardware de seguridad de Módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por un número de identificación personal (PIN) especificado por el usuario que se debe proporcionar al equipo en el inicio.<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Protege la clave de cifrado del volumen mediante el hardware de seguridad de Módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por un número de identificación personal (PIN) especificado por el usuario y por una clave externa que debe proporcionarse al equipo en el inicio.<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Protege la clave de cifrado del volumen mediante el hardware de seguridad de Módulo de plataforma segura (TPM) del equipo, si está disponible, mejorado por una clave externa que se debe proporcionar al equipo en el inicio.<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Reanuda el cifrado o descifrado de un volumen.<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Escribe la clave externa asociada al protector de clave de volumen especificado en una ubicación de archivo especificada.<br/>                                                                                                                                                                   |
| [**SetIdentificationField**](setidentificationfield-win32-encryptablevolume.md)                                         | Establece la cadena de identificador especificada en los metadatos del volumen.<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Usa el archivo de certificado proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Usa la huella digital del certificado proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Usa una clave externa proporcionada para acceder al contenido de un volumen de datos.<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Usa una contraseña numérica proporcionada para acceder al contenido de un volumen de datos.<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, la clave derivada se usa para desbloquear la clave maestra del volumen cifrado.<br/>                                                                                                                   |
| [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md)                                                           | Actualiza un volumen del formato Windows Vista al formato Windows 7.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **clase \_ EncryptableVolume de Win32** tiene estas propiedades.

<dl> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identificador único para el volumen en este sistema. Use esta opción para asociar un volumen a otras clases de proveedor WMI, por ejemplo, **volumen Win32 \_**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Letra de unidad del volumen. Este identificador se puede usar para asociar un volumen a otras clases de proveedor WMI, por [**ejemplo, volumen \_ Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)).

Para volúmenes sin letras de unidad, este valor es **NULL.**

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador persistente para el volumen en este sistema. Este identificador es exclusivo de **Win32 \_ EncryptableVolume.**

Este identificador es una cadena vacía si el volumen es un volumen NTFS estándar totalmente descifrado; de lo contrario, tiene un valor único.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado del volumen, independientemente de si BitLocker protege o no el volumen. Este valor se almacena cuando se crea una instancia de la clase . Es posible que el estado de protección cambie de estado entre la creación de instancias y cuando se comprueba el valor. Para comprobar el valor de la **propiedad ProtectionStatus** en tiempo real, use el [**método GetProtectionStatus.**](getprotectionstatus-win32-encryptablevolume.md)



| Valor                                                                        | Significado                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | PROTECCIÓN DESACTIVADA<br/> El volumen no está cifrado, parcialmente cifrado o la clave de cifrado del volumen para el volumen está disponible sin cifrar en el disco duro. <br/> |
| <dl> <dt>1</dt> </dl> | PROTECCIÓN ON<br/> El volumen está totalmente cifrado y la clave de cifrado del volumen no está disponible sin cifrar en el disco duro. <br/>                          |
| <dl> <dt>2</dt> </dl> | PROTECCIÓN DESCONOCIDA<br/> No se puede determinar el estado de protección del volumen. Una posible causa es que el volumen está en un estado bloqueado.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

La **clase de proveedor WMI \_ EncryptableVolume de Win32** se basa en la seguridad del espacio de nombres WMI y en el subsistema Cifrado de unidad BitLocker para el control de acceso.

Para usar los **\_ métodos EncryptableVolume de Win32,** se deben cumplir las condiciones siguientes:

-   Debe tener privilegios de administrador.
-   El cifrado de conexión debe poder conectarse al proveedor.

    Para obtener más información sobre cómo crear una conexión cifrada, vea [Requerir una conexión cifrada a un espacio de nombres](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md).

Para habilitar las conexiones remotas, se debe permitir el tráfico WMI remoto. Para obtener más información sobre cómo habilitar el tráfico WMI, vea [Conectarse a WMI de forma remota a partir de Vista](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md).

La configuración de seguridad del espacio de nombres predeterminado incluye una entrada para permitir la edición de forma predeterminada. Para obtener más información sobre la auditoría de espacios de nombres WMI, vea [Acceso a espacios de nombres WMI.](../wmisdk/access-to-wmi-namespaces.md)

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



 

 
