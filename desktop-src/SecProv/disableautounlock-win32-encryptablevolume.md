---
description: Quita la clave externa guardada en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Método DisableAutoUnlock de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: ce3a6bbb396136b128e084da0e64a79ad2f403217d8ac51dcf67b57941cc4a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004563"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método DisableAutoUnlock de la clase EncryptableVolume de Win32 \_

El método **DisableAutoUnlock** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) quita la clave externa guardada en el volumen del sistema operativo actualmente en ejecución para que un volumen de datos no se desbloquee automáticamente cuando se monta, como cuando los dispositivos de memoria extraíble están conectados al equipo.

Si el desbloqueo automático está deshabilitado o suspendido, se deben usar los métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para desbloquear el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                       | Método realizado correctamente.<br/>                                                       |
| <dl> <dt> **VOLUMEN \_ FVE E \_ \_ NO ENLAZADO \_ 2150694935**</dt> <dt>(0x80310017)</dt> </dl> | El desbloqueo automático en el volumen está deshabilitado.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | El método no se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>      |



 

## <a name="remarks"></a>Comentarios

Si no se devuelve ningún error, este método quita del registro los IDs de protector de volumen y las claves externas que se usan para desbloquear automáticamente el volumen.

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

 

 
