---
description: Comienza el cifrado de un volumen de sistema operativo completamente descifrado después de una prueba de hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Método EncryptAfterHardwareTest de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6421c054080e250bca4e673a66dcc4096a541519
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466452"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Método EncryptAfterHardwareTest de la clase EncryptableVolume de Win32 \_

El **método EncryptAfterHardwareTest** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) comienza el cifrado de un volumen de sistema operativo completamente descifrado después de una prueba de hardware. Se requiere un reinicio para realizar esta prueba de hardware. Use este método en lugar del [**método Encrypt**](encrypt-win32-encryptablevolume.md) para comprobar que BitLocker funcionará según lo previsto.

> [!Note]  
> Si la unidad de disco duro está cifrada por hardware, este método no cifra los datos. En su lugar, establece el estado de la banda en desbloqueado desde "desbloqueado permanentemente". Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncryptionMethod* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Especifica el algoritmo de cifrado y el tamaño de clave usados para cifrar el volumen. Deje este parámetro en blanco para usar el valor predeterminado de cero. Si el volumen está parcial o totalmente cifrado, el valor de este parámetro debe ser 0 o coincidir con el método de cifrado existente del volumen. Si la configuración directiva de grupo correspondiente se ha habilitado con un valor válido, el valor de este parámetro debe ser 0 o coincidir con directiva de grupo configuración.

Si la configuración directiva de grupo correspondiente no es válida, se usa el valor predeterminado de AES 128 con difusor.



| Valor                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**No especificado**</dt> <dt>0</dt> </dl> | Use la configuración de directiva de grupo actual, si está disponible y es válida, o bien el método de cifrado predeterminado en caso contrario.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 CON DIFUSOR<br/> Cifre el volumen mediante el algoritmo Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y con un tamaño de clave AES de 128 bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 CON DIFUSOR<br/> Cifre el volumen mediante el algoritmo Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y con un tamaño de clave AES de 256 bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Cifre el volumen mediante el algoritmo Estándar de cifrado avanzado (AES) y un tamaño de clave AES de 128 bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Cifre el volumen mediante el algoritmo Estándar de cifrado avanzado (AES) y un tamaño de clave AES de 256 bits.<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Marcas que describen el comportamiento de cifrado.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise y Windows Server 2008:** Este parámetro no está disponible.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realizar el cifrado de volumen en modo de cifrado solo de datos al iniciar el nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, al llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) se reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o **EncryptAfterHardwareTest** inician el cifrado desde el estado completamente descifrado, descifrado en estado en curso o estado en pausa de descifrado. Si este bit es cero, lo que significa que no está establecido, al iniciar el nuevo proceso de cifrado, se realizará la conversión en modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice el borrado a petición del espacio libre del volumen. Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o limpiando actualmente y está en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Realice la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el [**método Encrypt.**](encrypt-win32-encryptablevolume.md) Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado detenido o interrumpido o cuando el cifrado o el borrar están en curso. Esto permite que el autor de la llamada se reanude sincrónicamente esperando hasta que se complete o interrumpa el proceso.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Este método devuelve inmediatamente. Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve cero.




| Código o valor devuelto | Descripción | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Método realizado correctamente.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt><dt>2147942487 (0x80070057)</dt></dl> | Se proporciona el parámetro <em>EncryptionMethod,</em> pero no está dentro del intervalo conocido o no coincide con la configuración directiva de grupo actual.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt><dt>2150694958 (0x8031002E)</dt></dl> | No existe ninguna clave de cifrado para el volumen.<br /> Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar protectores de clave para el volumen:<ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> | 
| <dl><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt><dt>2150694942 (0x8031001E)</dt></dl> | El volumen no se puede cifrar porque este equipo está configurado para formar parte de un clúster de servidores.<br /> | 
| <dl><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt><dt>2150694971 (0x8031003B)</dt></dl> | No se pueden encontrar protectores de clave del tipo "TPM", "TPM y PIN", "TPM y PIN y clave de inicio", "TPM y clave de inicio" o "Clave externa". La prueba de hardware solo implica los protectores de clave anteriores.<br /> Si todavía desea ejecutar una prueba de hardware, debe usar uno de los métodos siguientes para especificar protectores de clave para el volumen:<ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> | 
| <dl><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt><dt>2150694969 (0x80310039)</dt></dl> | El volumen está parcial o totalmente cifrado.<br /> La prueba de hardware se aplica antes de que se produzca el cifrado. Si todavía desea ejecutar la prueba, use primero el método <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> y, a continuación, use uno de los métodos siguientes para agregar protectores de clave:<ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> | 
| <dl><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt><dt>2150694952 (0x80310028)</dt></dl> | El volumen es un volumen de datos.<br /> La prueba de hardware solo se aplica a los volúmenes que pueden iniciar el sistema operativo. Ejecute este método en el volumen del sistema operativo iniciado actualmente.<br /> | 
| <dl><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt><dt>2150694956 (0x8031002C)</dt></dl> | No se especifica ningún protector de clave del tipo "Contraseña numérica". El directiva de grupo requiere una copia de seguridad de la información de recuperación para Active Directory Domain Services. Para agregar al menos un protector de clave de ese tipo, use el <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>método ProtectKeyWithNumericalPassword.</strong></a><br /> | 




 

## <a name="remarks"></a>Comentarios

Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión de modo completo para mantener el comportamiento compatible con versiones anteriores. De este modo, la expectativa de seguridad de las aplicaciones y scripts existentes no se verá rota con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.

A diferencia [**del método Encrypt,**](encrypt-win32-encryptablevolume.md) este método hace lo siguiente:

-   Comprueba si el TPM podrá desbloquear el volumen, si existe un protector de clave relacionado con TPM.
-   Comprueba si el equipo puede leer una unidad flash USB que contiene un archivo de clave externa durante el inicio, si el volumen se desbloqueará mediante una clave externa (incluida una clave de inicio).
-   Requiere un reinicio del equipo para ejecutar la prueba de hardware.
-   Inicia el cifrado solo si la prueba de hardware se realiza correctamente.
-   No se puede usar en un volumen de datos, en un volumen parcial o totalmente cifrado, ni para reanudar el cifrado.

Antes de ejecutar este método, use los métodos siguientes para crear los protectores de clave relacionados:

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Después de ejecutar este método, siga estos pasos adicionales:

1.  Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa. Este paso solo se aplica si el volumen tiene un protector de clave de tipo "Clave externa" o "TPM y clave de inicio".
2.  Reinicie el equipo.

Al reiniciar el equipo, la prueba de hardware se ejecuta automáticamente.

El cifrado comienza si la prueba de hardware se realiza correctamente. De lo contrario, intente resolver los errores de hardware. Ejecute [**GetHardwareTestStatus después**](gethardwareteststatus-win32-encryptablevolume.md) de reiniciar el equipo para obtener los resultados de la prueba.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
