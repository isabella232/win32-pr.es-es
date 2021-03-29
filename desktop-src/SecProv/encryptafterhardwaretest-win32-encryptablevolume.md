---
description: Inicia el cifrado de un volumen del sistema operativo totalmente descifrado después de una prueba de hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Método EncryptAfterHardwareTest de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540942"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Método EncryptAfterHardwareTest de la \_ clase EncryptableVolume de Win32

El método **EncryptAfterHardwareTest** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) inicia el cifrado de un volumen del sistema operativo totalmente descifrado después de una prueba de hardware. Se requiere un reinicio para realizar esta prueba de hardware. Utilice este método en lugar del método [**Encrypt**](encrypt-win32-encryptablevolume.md) para comprobar que BitLocker funcionará según lo esperado.

> [!Note]  
> Si el disco duro está cifrado por hardware, este método no cifra los datos. En su lugar, establece el estado de la banda en desbloqueado de "sin bloqueos". Si la banda está bloqueada, desbloqueada o es de solo lectura, se considera que la unidad está cifrada.

 

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

Tipo: **UInt32**

Especifica el algoritmo de cifrado y el tamaño de la clave que se usa para cifrar el volumen. Deje este parámetro en blanco para usar el valor predeterminado de cero. Si el volumen está cifrado parcial o totalmente, el valor de este parámetro debe ser 0 o coincidir con el método de cifrado existente del volumen. Si se ha habilitado la configuración de directiva de grupo correspondiente con un valor válido, el valor de este parámetro debe ser 0 o coincidir con el valor directiva de grupo.

Si el valor de directiva de grupo correspondiente no es válido, se usa el valor predeterminado de AES 128 con difusor.



| Value                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> No <dt>**especificado**</dt> <dt>0</dt> </dl> | Use el valor de directiva de grupo actual, si está disponible y es válido, o el método de cifrado predeterminado de lo contrario.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 CON DIFUSOR<br/> Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y usando un tamaño de clave de AES de 128 bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 CON DIFUSOR<br/> Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor y usando un tamaño de clave de AES de 256 bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) y usando un tamaño de clave AES de 128 bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Cifre el volumen mediante el algoritmo de Estándar de cifrado avanzado (AES) y usando un tamaño de clave AES de 256 bits.<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[ en, opcional\]
</dt> <dd>

Tipo: **UInt32**

Marcas que describen el comportamiento de cifrado.

**Windows 7, Windows server 2008 R2, Windows Vista Enterprise y Windows server 2008:** Este parámetro no está disponible.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Value                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, la llamada al método de [**cifrado**](encrypt-win32-encryptablevolume.md) reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o **EncryptAfterHardwareTest** inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado. Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice un borrado a petición del espacio libre del volumen. Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Realizar la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el método [**Encrypt**](encrypt-win32-encryptablevolume.md) . Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso. Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Este método vuelve inmediatamente. Si el volumen ya está totalmente cifrado y no se devuelve ningún otro error, este método devuelve cero.



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
<td>No existe ninguna clave de cifrado para el volumen.<br/> Deshabilite los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o use uno de los métodos siguientes para especificar los protectores de clave para el volumen:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>No se puede cifrar el volumen porque este equipo está configurado para formar parte de un clúster de servidores.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </dl></td>
<td>No se puede encontrar ningún protector de clave del tipo &quot; TPM &quot; , &quot; TPM y PIN &quot; , &quot; TPM, PIN y clave &quot; de inicio, &quot; TPM y clave de inicio, &quot; o clave &quot; externa &quot; . La prueba de hardware solo implica los protectores de clave anteriores.<br/> Si todavía desea ejecutar una prueba de hardware, debe usar uno de los métodos siguientes para especificar los protectores de clave para el volumen:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>El volumen se ha cifrado parcial o totalmente.<br/> La prueba de hardware se aplica antes de que se produzca el cifrado. Si todavía desea ejecutar la prueba, use primero el método <a href="decrypt-win32-encryptablevolume.md"><strong>descifrado</strong></a> y, a continuación, use uno de los métodos siguientes para agregar protectores de clave:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>El volumen es un volumen de datos.<br/> La prueba de hardware solo se aplica a los volúmenes que pueden iniciar el sistema operativo. Ejecute este método en el volumen del sistema operativo iniciado actualmente.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>No se especifica ningún protector de clave de la &quot; contraseña numérica de tipo &quot; . El directiva de grupo requiere una copia de seguridad de la información de recuperación en Active Directory Domain Services. Para agregar al menos un protector de clave de ese tipo, utilice el método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Cuando se usa este método sin el segundo parámetro opcional (según la definición de Windows 7 y Windows Vista Enterprise), el método siempre iniciará la conversión de modo completo para mantener el comportamiento compatible con versiones anteriores. De este modo, la expectativa de seguridad de las aplicaciones y los scripts existentes no se interrumpirá con la adición del segundo parámetro opcional en Windows 8 y Windows Server 2012.

A diferencia del método [**Encrypt**](encrypt-win32-encryptablevolume.md) , este método hace lo siguiente:

-   Comprueba si el TPM podrá desbloquear el volumen, si existe un protector de clave relacionado con TPM.
-   Comprueba si el equipo puede leer una unidad flash USB que contenga un archivo de clave externa durante el inicio, en caso de que el volumen se desbloquee con una clave externa (incluida una clave de inicio).
-   Requiere un reinicio del equipo para ejecutar la prueba de hardware.
-   Inicia el cifrado solo si la prueba de hardware se realiza correctamente.
-   No se puede usar en un volumen de datos, en un volumen parcial o totalmente cifrado, o para reanudar el cifrado.

Antes de ejecutar este método, use los métodos siguientes para crear los protectores de clave relacionados:

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Después de ejecutar este método, siga estos pasos adicionales:

1.  Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa. Este paso solo se aplica si el volumen tiene un protector de clave de tipo "clave externa" o "TPM y clave de inicio".
2.  Reinicie el equipo.

En el reinicio del equipo, la prueba de hardware se ejecuta automáticamente.

El cifrado se inicia si la prueba de hardware se realiza correctamente. De lo contrario, intente resolver cualquier error de hardware. Ejecute [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) después de reiniciar el equipo para obtener los resultados de las pruebas.

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

 

 
