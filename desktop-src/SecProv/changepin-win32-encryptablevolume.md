---
description: Cambia el PIN asociado a un volumen cifrado.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Método ChangePIN de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540950"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Método ChangePIN de la \_ clase EncryptableVolume de Win32

El método **ChangePIN** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) cambia el PIN asociado a un volumen cifrado. Si está habilitada la Directiva de grupo "permitir PIN mejorados para el inicio", un PIN puede contener letras, símbolos y espacios, además de números.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*NewPIN* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena de identificación personal especificada por el usuario. Esta cadena debe estar formada por una secuencia de 4 a 20 dígitos o, si la Directiva de grupo "permitir PIN mejorados para el inicio" está habilitada, de 4 a 20 letras, símbolos, espacios o números.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ \_ CDDVD de arranque**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | En este equipo se encuentra un CD/DVD de arranque. Quite el CD o el DVD y reinicie el equipo.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ caracteres de PIN no válidos**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | El parámetro *NewPIN* contiene caracteres que no son válidos. Cuando el directiva de grupo "permitir PIN mejorados para el inicio" está deshabilitado, solo se admiten los números.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido </dl>     | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica" o "clave externa". Use el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Longitud de \_ \_ PIN no \_ válida de la Directiva E**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | El parámetro *NewPIN* proporcionado tiene más de 20 caracteres, menos de 4 caracteres, o menor que la longitud mínima especificada por directiva de grupo.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>        | El protector de clave proporcionado no existe en el volumen.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | No se encontró ningún Módulo de plataforma segura compatible (TPM) en este equipo.<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

El método **ChangePIN** crea un nuevo protector de TPM y PIN basado en la información del protector existente y en el PIN recién proporcionado. El nuevo protector tendrá el mismo GUID. También se puede llamar al método **ChangePIN** para cambiar el PIN de cualquier protector de clave que use un PIN, por ejemplo, TPM y PIN o TPM con PIN y USB.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
