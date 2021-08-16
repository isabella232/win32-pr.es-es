---
description: Indica si el contenido del volumen es accesible desde Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Método GetLockStatus de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: caa213dbebc7db07851bc8df41b5d9379d3dfe97ee207f9b2578b0567fd9b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892021"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetLockStatus de la clase EncryptableVolume de Win32 \_

El **método GetLockStatus** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el contenido del volumen es accesible desde Windows.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LockStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Especifica si el contenido del volumen es accesible desde Windows.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Desbloqueado**</dt> <dt>0</dt> </dl> | Para un HDD estándar:<br/> Se puede acceder al contenido completo del volumen. Un volumen desbloqueado se descifra completamente o tiene la clave de cifrado disponible en el disco. El volumen que contiene el sistema operativo en ejecución actual (por ejemplo, el volumen de Windows en ejecución) siempre es accesible y no se puede bloquear.<br/> Para un EHDD:<br/> La banda se desbloquea permanentemente.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Bloqueado**</dt> <dt>1</dt> </dl>         | Para un HDD estándar:<br/> No se puede acceder a todo o a una parte del contenido del volumen. Un volumen bloqueado debe estar parcial o totalmente cifrado y no debe tener la clave de cifrado disponible en el disco.<br/> Para un EHDD:<br/> La banda está desbloqueada o bloqueada.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Use [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) y [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para obtener acceso al contenido del volumen. Use el [**método Lock**](lock-win32-encryptablevolume.md) para volver a dar acceso al contenido del volumen.

El volumen que contiene el sistema operativo actualmente en ejecución siempre es accesible y no se puede bloquear.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, solo Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
