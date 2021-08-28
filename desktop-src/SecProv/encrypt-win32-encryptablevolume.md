---
description: Comienza el cifrado de un volumen totalmente descifrado o reanuda el cifrado de un volumen parcialmente cifrado.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Método Encrypt de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 968ff7f64a9a98a711210a4cfae64006c5a8f965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481031"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Método Encrypt de la clase EncryptableVolume de Win32 \_

El **método Encrypt** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) comienza el cifrado de un volumen completamente descifrado o reanuda el cifrado de un volumen parcialmente cifrado. Cuando el cifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Cuando el descifrado está en pausa o en curso, este método detiene el descifrado y comienza el cifrado.

> [!Note]  
> Si la unidad está cifrada por hardware, este método no cifra los datos. En su lugar, establece el estado de banda en "desbloqueado" desde "siempre desbloqueado". Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.

 

**Windows Vista:** No se admite el cifrado de un volumen distinto del volumen del sistema operativo que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncryptionMethod* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que especifica el algoritmo de cifrado y el tamaño de clave usados para cifrar el volumen. Si este parámetro es mayor que cero y el volumen está parcial o totalmente cifrado, *EncryptionMethod* debe coincidir con el método de cifrado existente del volumen. Si este parámetro es mayor que cero y la configuración de directiva de grupo correspondiente está habilitada con un valor válido, *EncryptionMethod* debe coincidir con la directiva de grupo configuración.

Para obtener una lista de los posibles valores de EncryptionMethod, vea el [**método GetEncryptionMethod.**](getencryptionmethod-win32-encryptablevolume.md)

El valor predeterminado de Windows 7 o inferior es: 1 (AES \_ 128 \_ WITH \_ DIFUSOR).

El valor predeterminado de Windows 8, Windows 8.1 o Windows 10 versión 1507 es: 3 (AES \_ 128).

El valor predeterminado de Windows 10 versión 1511 o posterior es: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Marcas que describen el comportamiento de cifrado.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise y Windows Server 2008:** Este parámetro no está disponible.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realizar el cifrado de volumen en modo de cifrado solo de datos al iniciar el nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, al llamar al método **Encrypt** se reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado desde el estado completamente descifrado, descifrado en estado en curso o estado en pausa de descifrado. Si este bit es cero, lo que significa que no está establecido, al iniciar el nuevo proceso de cifrado, se realizará la conversión en modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice el borrado a petición del espacio libre del volumen. Solo se permite llamar al método **Encrypt** con este conjunto de bits cuando el volumen no se está convirtiendo o limpiando actualmente y está en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Realice la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el **método Encrypt.** Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado detenido o interrumpido o cuando el cifrado o el borrar están en curso. Esto permite que el autor de la llamada se reanude sincrónicamente esperando hasta que se complete o interrumpa el proceso.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Este método devuelve inmediatamente. Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve 0.




| Código o valor devuelto | Descripción | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Método realizado correctamente.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt><dt>2147942487 (0x80070057)</dt></dl> | Se proporciona el parámetro <em>EncryptionMethod,</em> pero no está dentro del intervalo conocido o no coincide con la configuración directiva de grupo actual.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt><dt>2150694958 (0x8031002E)</dt></dl> | No existe ninguna clave de cifrado para el volumen. Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar protectores de clave para el volumen:<br /><ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><strong>Windows Vista:</strong> Cuando no existe ninguna clave de cifrado para el volumen, ERROR_INVALID_OPERATION se devuelve en su lugar. El valor decimal es 4317 y el valor hexadecimal es 0x10DD.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt><dt>2150694957 (0x8031002D)</dt></dl> | El método de cifrado proporcionado no coincide con el del volumen parcial o totalmente cifrado. Para continuar con el cifrado, deje el <em>parámetro EncryptionMethod</em> en blanco o use un valor de cero.<br /> | 
| <dl><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt><dt>2150694942 (0x8031001E)</dt></dl> | El volumen no se puede cifrar porque este equipo está configurado para formar parte de un clúster de servidores.<br /> | 
| <dl><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt><dt>2150694912 (0x80310000)</dt></dl> | El volumen está bloqueado.<br /> | 
| <dl><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt><dt>2150694956 (0x8031002C)</dt></dl> | No se especifica ningún protector de clave del tipo "Contraseña numérica". El directiva de grupo requiere una copia de seguridad de la información de recuperación para Active Directory Domain Services. Para agregar al menos un protector de clave de ese tipo, use el <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>método ProtectKeyWithNumericalPassword.</strong></a><br /> | 




 

## <a name="remarks"></a>Comentarios

Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión en modo completo para mantener el comportamiento compatible con versiones anteriores. De este modo, la expectativa de seguridad de las aplicaciones y scripts existentes no se verá rota con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.

Puede llamar a [**GetConversionStatus para**](getconversionstatus-win32-encryptablevolume.md) determinar si el cifrado está en curso y el porcentaje del volumen que se ha cifrado.

Una vez que el volumen está totalmente cifrado y si se han agregado y habilitado protectores de clave, el estado de protección del volumen cambia a "activado".

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
