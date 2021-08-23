---
description: Quita todas las claves externas y la información relacionada guardada en el volumen del sistema operativo que se ejecuta actualmente y que se usa para desbloquear automáticamente los volúmenes de datos.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668175"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Método ClearAllAutoUnlockKeys de la clase EncryptableVolume de Win32 \_

El **método ClearAllAutoUnlockKeys** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita todas las claves externas y la información relacionada guardada en el volumen del sistema operativo en ejecución que se usa para desbloquear automáticamente los volúmenes de datos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>     |



 

## <a name="remarks"></a>Comentarios

**ClearAllAutoUnlockKeys** logra la misma funcionalidad que la ejecución de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para todos los volúmenes de datos que se hayan asociado alguna vez al sistema operativo actualmente en ejecución, incluso los volúmenes de datos que no están conectados actualmente al equipo. También quita cualquier información de desbloqueo obsoleta asociada a volúmenes de datos que ya no existen.

Antes de llamar a [**Decrypt**](decrypt-win32-encryptablevolume.md) en el volumen del sistema operativo que se está ejecutando actualmente, use **ClearAllAutoUnlockKeys** para asegurarse de que la información colocada en el registro del sistema operativo para desbloquear automáticamente los volúmenes de datos no sea accesible en el disco.

Una **vez que ClearAllAutoUnlockKeys** se ejecuta correctamente, se pueden usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear todos los volúmenes de datos de este equipo. Use [**EnableAutoUnlock para**](enableautounlock-win32-encryptablevolume.md) volver a habilitar el desbloqueo automático de un volumen de datos.

Si no se devuelve ningún otro error, **ClearAllAutoUnlockKeys** quita del registro los iDs de protector de volumen y las claves externas que se usan para desbloquear automáticamente cualquier volumen de datos que se haya asociado con el volumen del sistema operativo que se está ejecutando actualmente.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, solo Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
