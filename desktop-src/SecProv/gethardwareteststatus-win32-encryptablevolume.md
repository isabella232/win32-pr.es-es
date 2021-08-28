---
description: Proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Método GetHardwareTestStatus de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 32d0d477459dbc7352d1d8f6779c5c76cfbd537d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475361"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareTestStatus de la clase EncryptableVolume de Win32 \_

El **método GetHardwareTestStatus** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) proporciona información de estado sobre una prueba de hardware de un volumen de sistema operativo completamente descifrado.

Use este método para mostrar si una prueba de hardware está pendiente, así como el éxito o el error de una prueba de hardware que se completó en el último reinicio del equipo. Para solicitar una prueba de hardware, use el [**método EncryptAfterHardwareTest.**](encryptafterhardwaretest-win32-encryptablevolume.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TestStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Especifica si hay una prueba de hardware pendiente, así como si se ha realizado correctamente una prueba de hardware que se completó en el último reinicio del equipo.




| Valor | Significado | 
|-------|---------|
| <span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl><dt><strong>NotFailed_and_NonePending</strong></dt><dt>0</dt></dl> | Si se solicitó una prueba, la prueba se ha hecho correctamente en el último reinicio del equipo y el cifrado del volumen está ahora en curso. Para conocer el estado de cifrado, consulte el <a href="getconversionstatus-win32-encryptablevolume.md"><strong>método GetConversionStatus.</strong></a> De lo contrario, no se ejecutó ninguna prueba en el último reinicio del equipo y no hay ninguna pendiente. <br /> | 
| <span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl><dt><strong>Error</strong></dt><dt>1</dt></dl> | No se hizo el cifrado del volumen. Se quitaron todos los protectores de clave.<br /> Para resolver una prueba con errores:<br /><ul><li>Consulte la información del <em>parámetro TestError.</em></li><li>Agregue protectores de clave y vuelva a usar <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>el método EncryptAfterHardwareTest.</strong></a></li></ul> | 
| <span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl><dt><strong>Pendiente</strong></dt><dt>2</dt></dl> | Se ha solicitado una prueba y se ejecutará en el siguiente reinicio del equipo.<br /> | 




 

</dd> <dt>

*TestError* \[ out\]
</dt> <dd>

Tipo: **uint32**

Especifica el error de la última prueba de hardware completada.



| Valor                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | No se produjo ningún error o no se ejecutó ninguna prueba de hardware en el último reinicio del equipo.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | NO SE ENCONTRÓ EL ARCHIVO DE CLAVE DE FVE \_ \_ \_ E \_<br/> No se encontró una unidad flash USB con un archivo de clave externa. Si este error persiste, el equipo no puede leer unidades USB durante el reinicio. Es posible que no pueda usar claves externas para desbloquear el volumen del sistema operativo durante el reinicio.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ KEYFILE \_ INVALID<br/> El archivo de clave externa de la unidad flash USB estaba dañado. Pruebe otra unidad flash USB para almacenar el archivo de clave externa.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | TPM de FVE \_ E \_ \_ DESHABILITADO<br/> El TPM está deshabilitado o desactivado o deshabilitado y desactivado. Para activar el TPM, use el proveedor WMI de Tpm [**Win32 \_**](win32-tpm.md) o ejecute el complemento de administración de TPM (Tpm.msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | PCR \_ no válido del TPM \_ \_ \_ de FVE E<br/> El TPM detectó un cambio en los servicios de reinicio del sistema operativo dentro del perfil de validación de la plataforma actual. Quite cualquier CD o DVD de inicio del equipo. Si este error persiste, compruebe que están instaladas las actualizaciones más recientes del bios y el firmware y que el TPM funciona correctamente.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | EL PIN E de FVE \_ \_ NO ES \_ VÁLIDO<br/> El PIN proporcionado era incorrecto.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                  | Descripción                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | El método se ha llevado a cabo de forma correcta.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl> | El volumen está bloqueado.<br/> |



 

## <a name="remarks"></a>Comentarios

Para solicitar una prueba de hardware, use el [**método EncryptAfterHardwareTest.**](encryptafterhardwaretest-win32-encryptablevolume.md)

Para ejecutar una prueba de hardware cuando su estado está pendiente, siga estos pasos:

1.  Inserte en el equipo una unidad flash USB que contenga un archivo de clave externa. Este paso solo se aplica si el volumen tiene un protector de clave de tipo "Clave externa" o "TPM y clave de inicio".
2.  Reinicie el equipo. Al reiniciar el equipo, la prueba de hardware se ejecuta automáticamente.

Para cancelar la prueba de hardware, use el [**método Encrypt.**](encrypt-win32-encryptablevolume.md)

Una prueba correcta determina que:

-   El TPM puede desbloquear el volumen si existe un protector de clave relacionado con TPM.
-   El equipo puede leer una unidad flash USB que contiene un archivo de clave externa durante el inicio si el volumen se puede desbloquear mediante una clave externa (incluida una clave de inicio).

Los resultados de las pruebas de hardware no estarán disponibles después de los cambios en la conversión o después del siguiente reinicio del equipo. Compruebe el registro de eventos del sistema para obtener información sobre las pruebas de hardware que se ejecutaban anteriormente en el equipo.

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

 

 
