---
description: Quita todas las claves externas y la información relacionada guardadas en el volumen del sistema operativo que se está ejecutando actualmente y que se usan para desbloquear automáticamente los volúmenes de datos.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686662"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Método ClearAllAutoUnlockKeys de la \_ clase EncryptableVolume de Win32

El método **ClearAllAutoUnlockKeys** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita todas las claves externas y la información relacionada guardadas en el volumen del sistema operativo que se está ejecutando actualmente y que se usan para desbloquear automáticamente los volúmenes de datos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ no es el \_ \_ volumen de sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>     |



 

## <a name="remarks"></a>Observaciones

**ClearAllAutoUnlockKeys** logra la misma funcionalidad que la ejecución de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para cada volumen de datos que se haya asociado al sistema operativo que se está ejecutando en ese momento, incluso a los volúmenes de datos que no están conectados al equipo. También quita cualquier información de desbloqueo obsoleta asociada a los volúmenes de datos que ya no existen.

Antes de llamar a [**descifrado**](decrypt-win32-encryptablevolume.md) en el volumen del sistema operativo que se está ejecutando actualmente, use **ClearAllAutoUnlockKeys** para asegurarse de que no se pueda tener acceso a la información colocada en el registro del sistema operativo para desbloquear automáticamente los volúmenes de datos sin cifrar en el disco.

Una vez que **ClearAllAutoUnlockKeys** se ejecuta correctamente, se pueden usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear todos los volúmenes de datos de este equipo. Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para volver a habilitar el desbloqueo automático de un volumen de datos.

Si no se devuelve ningún otro error, **ClearAllAutoUnlockKeys** quita del registro todos los identificadores de protector de volumen y las claves externas usadas para desbloquear automáticamente cualquier volumen de datos que se haya asociado al volumen del sistema operativo que se está ejecutando.

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

 

 
