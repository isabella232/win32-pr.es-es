---
description: Protege la clave de cifrado del volumen con una clave externa de 256 bits.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Método ProtectKeyWithExternalKey de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686640"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithExternalKey de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen con una clave externa de 256 bits. Esta clave externa se puede usar para recuperarse de los errores de autenticación de otros protectores de clave (por ejemplo, TPM).

Use el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para guardar esta clave externa en un archivo. Los dispositivos de memoria USB que contienen esta clave externa se pueden usar como una clave de inicio o una clave de recuperación cuando se inicia el equipo.

Se crea un protector de clave de tipo "clave externa" para el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que especifica un identificador asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se utiliza un valor en blanco.

</dd> <dt>

*ExternalKey* \[ en, opcional\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen.

Si no se especifica ninguna clave externa, se genera una de forma aleatoria. Use el método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obtener la clave generada de forma aleatoria.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Se proporciona el parámetro *ExternalKey* , pero no es una matriz de tamaño 4.<br/>            |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                                             |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/> |



 

## <a name="remarks"></a>Observaciones

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

 

 
