---
description: Elimina todos los protectores de clave del volumen.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors de la Win32_EncryptableVolume clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160700"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtectors de la clase EncryptableVolume de Win32 \_

El **método DeleteKeyProtectors** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) elimina todos los protectores de clave del volumen.

Si un volumen sin cifrar tiene protectores de clave, cuando **DeleteKeyProtectors** se ejecuta correctamente, el volumen vuelve a un sistema de archivos NTFS estándar.

Si el volumen aún no está descifrado por completo, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de ejecutar **DeleteKeyProtectors** para asegurarse de que las partes cifradas del volumen permanecen accesibles.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                          | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>         | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ KEY \_ REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | El último protector de clave para un volumen parcial o totalmente cifrado no se puede quitar si están habilitados los protectores de clave. Use [**DisableKeyProtectors antes**](disablekeyprotectors-win32-encryptablevolume.md) de quitar este último protector de clave para asegurarse de que las partes cifradas del volumen permanecen accesibles. <br/> |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ BOUND \_ ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Los protectores de clave no se pueden eliminar porque uno de ellos se usa para desbloquear automáticamente el volumen. <br/> Use [**DisableAutoUnlock para**](disableautounlock-win32-encryptablevolume.md) deshabilitar el desbloqueo automático antes de ejecutar este método.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
