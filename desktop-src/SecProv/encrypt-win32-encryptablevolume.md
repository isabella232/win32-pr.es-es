---
description: Inicia el cifrado de un volumen totalmente descifrado o reanuda el cifrado de un volumen parcialmente cifrado.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Método Encrypt de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083342"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Método Encrypt de la \_ clase Win32 EncryptableVolume

El método **Encrypt** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inicia el cifrado de un volumen totalmente descifrado o reanuda el cifrado de un volumen parcialmente cifrado. Cuando el cifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Cuando el descifrado está en pausa o en curso, este método detiene el descifrado y comienza el cifrado.

> [!Note]  
> Si la unidad está cifrada por hardware, este método no cifra los datos. En su lugar, establece el estado de la banda en "desbloqueado" de "siempre desbloqueado". Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.

 

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

Tipo: **UInt32**

Entero sin signo que especifica el algoritmo de cifrado y el tamaño de la clave que se usa para cifrar el volumen. Si este parámetro es mayor que cero y el volumen se ha cifrado parcial o totalmente, *EncryptionMethod* debe coincidir con el método de cifrado existente del volumen. Si este parámetro es mayor que cero y el valor de directiva de grupo correspondiente está habilitado con un valor válido, *EncryptionMethod* debe coincidir con la configuración de directiva de grupo.

Para obtener una lista de posibles valores de EncryptionMethod, consulte el método [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .

El valor predeterminado para Windows 7 o inferior es: 1 (AES \_ 128 \_ con \_ difusor).

El valor predeterminado para Windows 8, Windows 8.1 o Windows 10, versión 1507 es: 3 (AES \_ 128).

El valor predeterminado de Windows 10, versión 1511 o superior es: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ en, opcional\]
</dt> <dd>

Tipo: **UInt32**

Marcas que describen el comportamiento de cifrado.

**Windows 7, Windows server 2008 R2, Windows Vista Enterprise y Windows server 2008:** Este parámetro no está disponible.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Value                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, la llamada al método de **cifrado** reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado. Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice un borrado a petición del espacio libre del volumen. Solo se permite llamar al método **Encrypt** con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Realizar la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el método **Encrypt** . Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso. Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Este método vuelve inmediatamente. Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve 0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código o valor devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0X0)</dt> </dl></td>
<td>Método realizado correctamente.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>Se proporciona el parámetro <em>EncryptionMethod</em> , pero no está dentro del intervalo conocido o no coincide con el valor de directiva de grupo actual.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>No existe ninguna clave de cifrado para el volumen. Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar los protectores de clave para el volumen:<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista:</strong> Cuando no existe ninguna clave de cifrado para el volumen, se devuelve ERROR_INVALID_OPERATION en su lugar. El valor decimal es 4317 y el valor hexadecimal es 0x10DD.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </dl></td>
<td>El método de cifrado proporcionado no coincide con el del volumen totalmente cifrado o parcial. Para continuar con el cifrado, deje en blanco el parámetro <em>EncryptionMethod</em> o use un valor de cero.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>No se puede cifrar el volumen porque este equipo está configurado para formar parte de un clúster de servidores.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>El volumen está bloqueado.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>No se especifica ningún protector de clave de la &quot; contraseña numérica de tipo &quot; . El directiva de grupo requiere una copia de seguridad de la información de recuperación en Active Directory Domain Services. Para agregar al menos un protector de clave de ese tipo, utilice el método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión de modo completo para mantener el comportamiento compatible con versiones anteriores. De este modo, la expectativa de seguridad de las aplicaciones y los scripts existentes no se interrumpirá con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.

Puede llamar a [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) para determinar si el cifrado está en curso y el porcentaje del volumen que se ha cifrado.

Una vez que el volumen está totalmente cifrado y se han agregado y habilitado protectores de clave, el estado de protección del volumen cambia a "activado".

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]<br/>                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
