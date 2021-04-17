---
description: Elimina todos los protectores de clave para el volumen.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687571"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtectors de la \_ clase EncryptableVolume de Win32

El método **DeleteKeyProtectors** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina todos los protectores de clave para el volumen.

Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtectors** se ejecuta correctamente, el volumen se revierte a un sistema de archivos NTFS estándar.

Si el volumen no se ha descifrado completamente, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de ejecutar **DeleteKeyProtectors** para asegurarse de que las partes cifradas del volumen permanecen accesibles.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                          | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ clave \_ necesaria**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | No se puede quitar el último protector de clave para un volumen totalmente cifrado o parcial si están habilitados los protectores de clave. Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de quitar este protector de clave más reciente para asegurarse de que las partes cifradas del volumen sigan siendo accesibles. <br/> |
| <dl> <dt>**FVE \_ E \_ \_ enlazado \_ a un volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Los protectores de clave no se pueden eliminar porque se está usando uno de ellos para desbloquear automáticamente el volumen. <br/> Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para deshabilitar el desbloqueo automático antes de ejecutar este método.<br/>                                                       |



 

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

 

 
