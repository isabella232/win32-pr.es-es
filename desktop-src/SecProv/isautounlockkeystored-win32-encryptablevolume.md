---
description: Indica si las claves externas o la información relacionada que se puede usar para desbloquear automáticamente los volúmenes de datos existen en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688150"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockKeyStored de la \_ clase EncryptableVolume de Win32

El método **IsAutoUnlockKeyStored** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si existe cualquier clave externa o información relacionada que pueda usarse para desbloquear automáticamente los volúmenes de datos en el volumen del sistema operativo que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsAutoUnlockKeyStored* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

Es **true** si cualquier información que se pueda utilizar para desbloquear automáticamente los volúmenes de datos se almacena en el registro del volumen del sistema operativo que se está ejecutando actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ no es el \_ \_ volumen de sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>     |



 

## <a name="remarks"></a>Observaciones

Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para quitar toda la información de desbloqueo del volumen del sistema operativo que se está ejecutando actualmente.

La información que se usa para desbloquear un volumen se almacena cuando se ejecuta [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para un volumen de datos mientras se ejecuta el volumen del sistema operativo que se está ejecutando actualmente.

**IsAutoUnlockKeyStored** difiere de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) en que, aunque el desbloqueo automático esté deshabilitado para todos los volúmenes de datos conectados actualmente al equipo, puede que todavía esté desbloqueando la información asociada a los volúmenes de datos desconectados o volúmenes de datos que ya no existen.

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

 

 
