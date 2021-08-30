---
description: Cambia el PIN asociado a un volumen cifrado.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Método ChangePIN de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 009e3dde487bb28a5c99ffb62752ddee57c4a14f336c72fe4577131f3ab3ee6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035035"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Método ChangePIN de la clase EncryptableVolume de Win32 \_

El **método ChangePIN** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) cambia el PIN asociado a un volumen cifrado. Si la directiva de grupo "Permitir PIN mejorados para el inicio" está habilitada, un PIN puede contener letras, símbolos y espacios además de números.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*NewPIN* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena de identificación personal especificada por el usuario. Esta cadena debe constar de una secuencia de 4 a 20 dígitos o, si la directiva de grupo "Permitir PIN mejorados para el inicio" está habilitada, de 4 a 20 letras, símbolos, espacios o números.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                                | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | En este equipo se encuentra un CD/DVD de arranque. Quite el CD/DVD y reinicie el equipo.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ CARACTERES DE PIN NO \_ \_ VÁLIDOs**</dt> 2150695066 <dt>(0x8031009A)</dt> </dl>          | El *parámetro NewPIN* contiene caracteres que no son válidos. Cuando la opción "Permitir PIN mejorados para el inicio" directiva de grupo deshabilita, solo se admiten números.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ TIPO DE PROTECTOR \_ \_ NO**</dt> <dt>VÁLIDO 2150694970 (0x8031003A)</dt> </dl>     | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Contraseña numérica" o "Clave externa". Use el [**método ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>               | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY INVALID PIN LENGTH \_ \_ \_ 2150695016**</dt> <dt>(0x80310068)</dt> </dl> | El *parámetro NewPIN* proporcionado tiene más de 20 caracteres, menos de 4 caracteres o más corto que la longitud mínima especificada por directiva de grupo.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ NO \_ SE \_ ENCONTRÓ \_ EL**</dt> <dt>PROTECTOR 2150694963 (0x80310033)</dt> </dl>        | El protector de clave proporcionado no existe en el volumen.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | No se encuentra Módulo de plataforma segura (TPM) compatible en este equipo.<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Comentarios

El **método ChangePIN** crea un nuevo protector de TPM y PIN basado en la información del protector existente y el PIN recién proporcionado. El nuevo protector tendrá el mismo GUID. También se puede llamar al método **ChangePIN** para cambiar el PIN de cualquier protector de clave que use un PIN, por ejemplo, TPM y PIN o TPM con PIN y USB.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de escritorio Ultimate \[\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
