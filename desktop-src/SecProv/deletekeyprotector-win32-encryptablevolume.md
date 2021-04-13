---
description: Elimina un protector de clave determinado para el volumen.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Método DeleteKeyProtector de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360214"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtector de la \_ clase EncryptableVolume de Win32

El método **DeleteKeyProtector** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina un protector de clave determinado para el volumen.

Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtector** quita el último protector de clave, el volumen se revierte a un sistema de archivos NTFS estándar.

Si nunca se ha cifrado un volumen, la eliminación del protector de clave revertirá a NTFS.

Si el volumen no se ha descifrado por completo, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar el último protector de clave del volumen para asegurarse de que las partes cifradas del volumen sigan siendo accesibles.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                          | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>         | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                  | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave válido.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ clave \_ necesaria**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | No se puede quitar el último protector de clave para un volumen totalmente cifrado o parcial si están habilitados los protectores de clave. Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar este protector de clave más reciente para asegurarse de que las partes cifradas del volumen sigan siendo accesibles. <br/> |
| <dl> <dt>**FVE \_ E \_ \_ enlazado \_ a un volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Este protector de clave no se puede eliminar porque se está usando para desbloquear automáticamente el volumen. <br/> Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para deshabilitar el desbloqueo automático antes de eliminar este protector de clave.<br/>                                                    |



 

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

 

 
