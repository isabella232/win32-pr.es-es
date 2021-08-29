---
description: Elimina un protector de clave determinado para el volumen.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Método DeleteKeyProtector de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e54e857e9aafda94878b3219209ee0cda65789cd408ed115c5d0f088f7907822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668065"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtector de la clase EncryptableVolume de Win32 \_

El **método DeleteKeyProtector** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina un protector de clave determinado para el volumen.

Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtector** quita el último protector de clave, el volumen vuelve a un sistema de archivos NTFS estándar.

Si nunca se ha cifrado un volumen, la eliminación del protector de clave se revertirá a NTFS.

Si el volumen aún no está completamente descifrado, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar el último protector de clave del volumen para asegurarse de que las partes cifradas del volumen siguen siendo accesibles.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                          | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>         | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                  | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave válido.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ KEY \_ REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | El último protector de clave para un volumen parcial o totalmente cifrado no se puede quitar si están habilitados los protectores de clave. Use [**DisableKeyProtectors antes**](disablekeyprotectors-win32-encryptablevolume.md) de quitar este último protector de clave para asegurarse de que las partes cifradas del volumen permanecen accesibles. <br/> |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ BOUND \_ ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Este protector de clave no se puede eliminar porque se usa para desbloquear automáticamente el volumen. <br/> Use [**DisableAutoUnlock para**](disableautounlock-win32-encryptablevolume.md) deshabilitar el desbloqueo automático antes de eliminar este protector de clave.<br/>                                                    |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
