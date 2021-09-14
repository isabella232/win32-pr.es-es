---
description: Indica si existen claves externas o información relacionada que se pueda usar para desbloquear automáticamente los volúmenes de datos en el volumen del sistema operativo que se está ejecutando actualmente.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored de la Win32_EncryptableVolume clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374866"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockKeyStored de la clase EncryptableVolume de Win32 \_

El **método IsAutoUnlockKeyStored** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si existen claves externas o información relacionada que se pueda usar para desbloquear automáticamente los volúmenes de datos en el volumen del sistema operativo que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsAutoUnlockKeyStored* \[ out\]
</dt> <dd>

Tipo: **booleano**

Es **true** si cualquier información que se pueda usar para desbloquear automáticamente volúmenes de datos se almacena en el registro del volumen del sistema operativo que se está ejecutando actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | El método solo se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>     |



 

## <a name="remarks"></a>Observaciones

Use [**ClearAllAutoUnlockKeys para**](clearallautounlockkeys-win32-encryptablevolume.md) quitar toda la información de desbloqueo del volumen del sistema operativo que se está ejecutando actualmente.

La información que se usa para desbloquear un volumen se almacena cuando se ejecuta [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para un volumen de datos mientras se ejecuta el volumen del sistema operativo en ejecución.

**IsAutoUnlockKeyStored** difiere de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) en que incluso si el desbloqueo automático está deshabilitado para todos los volúmenes de datos conectados actualmente al equipo, todavía puede haber información de desbloqueo asociada a volúmenes de datos desconectados o volúmenes de datos que ya no existen.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
