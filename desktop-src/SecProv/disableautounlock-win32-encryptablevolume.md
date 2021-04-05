---
description: Quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Método DisableAutoUnlock de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910053"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método DisableAutoUnlock de la \_ clase EncryptableVolume de Win32

El método **DisableAutoUnlock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando en ese momento, de modo que un volumen de datos no se desbloquee automáticamente cuando se monta, como cuando los dispositivos de memoria extraíbles están conectados al equipo.

Si el desbloqueo automático está deshabilitado o suspendido, se deben usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                       | Método realizado correctamente.<br/>                                                       |
| <dl> <dt> **FVE \_ E \_ volumen \_ no \_ enlazado**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | El desbloqueo automático en el volumen está deshabilitado.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.<br/>      |



 

## <a name="remarks"></a>Observaciones

Si no se devuelve ningún error, este método quita del registro todos los identificadores de protector de volumen y las claves externas usadas para desbloquear automáticamente el volumen.

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

 

 
