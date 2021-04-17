---
description: Indica si el contenido del volumen es accesible desde Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Método GetLockStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686648"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetLockStatus de la \_ clase EncryptableVolume de Win32

El método **GetLockStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el contenido del volumen es accesible desde Windows.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LockStatus* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Especifica si el contenido del volumen es accesible desde Windows.



| Value                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Desbloqueado**</dt> <dt>0</dt> </dl> | Para una unidad de disco duro estándar:<br/> Se puede tener acceso al contenido completo del volumen. Un volumen desbloqueado es totalmente descifrado o tiene la clave de cifrado disponible en el disco sin cifrar. El volumen que contiene el sistema operativo en ejecución actual (por ejemplo, el volumen de Windows en ejecución) siempre es accesible y no se puede bloquear.<br/> Para un EHDD:<br/> La banda se desbloquea de forma perpetua.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Bloqueado**</dt> <dt>1</dt> </dl>         | Para una unidad de disco duro estándar:<br/> No se puede tener acceso a todo o una parte del contenido del volumen. Un volumen bloqueado debe estar cifrado parcial o totalmente y no debe tener la clave de cifrado disponible en el disco sin cifrar.<br/> Para un EHDD:<br/> La banda está desbloqueada o bloqueada.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Use [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) y [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para obtener acceso al contenido del volumen. Use el método [**Lock**](lock-win32-encryptablevolume.md) para ceder el acceso al contenido del volumen.

El volumen que contiene el sistema operativo que se está ejecutando actualmente siempre es accesible y no se puede bloquear.

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

 

 
