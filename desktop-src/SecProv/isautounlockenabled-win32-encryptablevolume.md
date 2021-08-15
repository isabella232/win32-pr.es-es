---
description: Indica si el volumen se desbloquea automáticamente cuando se monta.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Método IsAutoUnlockEnabled de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 19437bf40d27bea87103beecfbe8bee71e404c054ace46cb9728f7ac992b5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891916"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockEnabled de la clase EncryptableVolume de Win32 \_

El **método IsAutoUnlockEnabled** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen se desbloquea automáticamente cuando se monta (por ejemplo, cuando los dispositivos de memoria extraíbles están conectados al equipo).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsAutoUnlockEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Valor booleano que es true si la clave externa usada para desbloquear automáticamente el volumen existe y se ha almacenado en el volumen del sistema operativo que se está ejecutando actualmente; de lo contrario, es false.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que contiene el identificador del protector de clave de volumen cifrado asociado si *IsAutoUnlockEnabled* es true.

Si *IsAutoUnlockEnabled* es false, *VolumeKeyProtectorID* es una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                     | Descripción                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                     | Método realizado correctamente.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | El método no se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>      |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
