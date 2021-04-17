---
description: Proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Método GetHardwareTestStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688161"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareTestStatus de la \_ clase EncryptableVolume de Win32

El método **GetHardwareTestStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.

Use este método para mostrar si hay una prueba de hardware pendiente, así como el éxito o el fracaso de una prueba de hardware completada en el último reinicio del equipo. Para solicitar una prueba de hardware, use el método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TestStatus* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Especifica si hay una prueba de hardware pendiente, así como el éxito del error de una prueba de hardware completada en el último reinicio del equipo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </dl></td>
<td>Si se solicitó una prueba, la prueba se realizó correctamente en el último reinicio del equipo y el cifrado del volumen ya está en curso. Para obtener el estado de cifrado, consulte el método <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> . De lo contrario, no se ejecutó ninguna prueba en el último reinicio del equipo y no hay ninguna pendiente. <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <dt><strong>Error</strong></dt> <dt>1</dt> </dl></td>
<td>No se inició el cifrado de volumen. Se quitaron todos los protectores de clave.<br/> Para resolver una prueba con errores:<br/>
<ul>
<li>Consulte la información del parámetro <em>TestError</em> .</li>
<li>Agregue protectores de clave y vuelva a usar el método <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <dt><strong>Pendiente</strong></dt> <dt>2</dt> </dl></td>
<td>Se ha solicitado una prueba que se ejecutará en el próximo reinicio del equipo.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*TestError* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Especifica el error de la última prueba de hardware completada.



| Value                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | No se ha producido ningún error o no se ejecutó ninguna prueba de hardware en el último reinicio del equipo.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | \_ \_ \_ no \_ se encontró FVE E keyfile<br/> No se encontró una unidad flash USB con un archivo de clave externa. Si el error persiste, el equipo no podrá leer las unidades USB durante el reinicio. Es posible que no pueda usar claves externas para desbloquear el volumen del sistema operativo durante el reinicio.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ keyfile \_ no válido<br/> El archivo de clave externa en la unidad flash USB estaba dañado. Pruebe una unidad flash USB diferente para almacenar el archivo de clave externa.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ deshabilitado<br/> El TPM está deshabilitado o desactivado, o bien deshabilitado y desactivado. Para activar el TPM, use el proveedor [**WMI \_ TPM de Win32**](win32-tpm.md) o ejecute el complemento Administración de TPM (TPM. msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | \_ \_ \_ PCR no válido de FVE E TPM \_<br/> El TPM detectó un cambio en los servicios de reinicio del sistema operativo en el perfil de validación de plataforma actual. Quite cualquier CD o DVD de inicio del equipo. Si el error persiste, compruebe que las actualizaciones de firmware y BIOS más recientes están instaladas y que el TPM está funcionando correctamente.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | FVE \_ E \_ PIN \_ no válido<br/> El PIN proporcionado era incorrecto.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                  | Descripción                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | El método se ha llevado a cabo de forma correcta.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/> |



 

## <a name="remarks"></a>Observaciones

Para solicitar una prueba de hardware, use el método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

Para ejecutar una prueba de hardware cuando su estado es pendiente, siga estos pasos:

1.  Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa. Este paso solo se aplica si el volumen tiene un protector de clave de tipo "clave externa" o "TPM y clave de inicio".
2.  Reinicie el equipo. En el reinicio del equipo, la prueba de hardware se ejecuta automáticamente.

Para cancelar la prueba de hardware, use el método [**Encrypt**](encrypt-win32-encryptablevolume.md) .

Una prueba correcta determina que:

-   El TPM puede desbloquear el volumen si existe un protector de clave relacionado con TPM.
-   El equipo puede leer una unidad flash USB que contenga un archivo de clave externa durante el inicio si el volumen se puede desbloquear mediante una clave externa (incluida una clave de inicio).

Los resultados de la prueba de hardware no estarán disponibles después de realizar cambios en la conversión o después del siguiente reinicio del equipo. Compruebe el registro de eventos del sistema para obtener información acerca de las pruebas de hardware que se ejecutaron previamente en el equipo.

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

 

 
