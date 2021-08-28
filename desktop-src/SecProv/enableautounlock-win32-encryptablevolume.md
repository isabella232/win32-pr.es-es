---
description: Permite desbloquear automáticamente un volumen de datos cuando se monta el volumen.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Método EnableAutoUnlock de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 712a5460769009f9e10e2b9730ad78632bc5ad10c2af2d1eaf63bcb2c91d7c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892463"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método EnableAutoUnlock de la clase EncryptableVolume de Win32 \_

El **método EnableAutoUnlock** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) permite desbloquear automáticamente un volumen de datos cuando se monta el volumen.

El desbloqueo automático guarda una clave externa en el sistema operativo que puede desbloquear automáticamente el volumen en el volumen del sistema operativo que se está ejecutando actualmente.

Para usar este método, el volumen del sistema operativo ya debe estar protegido por Cifrado de unidad BitLocker o debe tener cifrado en curso. Además, ya debe existir una clave externa para el volumen de datos. Use [**ProtectKeyWithExternalKey para**](protectkeywithexternalkey-win32-encryptablevolume.md) crear la clave externa que puede desbloquear automáticamente el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica el protector de clave del tipo "External Key" que se usa para desbloquear automáticamente el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                           | Método realizado correctamente.<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>          | El volumen está bloqueado.<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave válido del tipo "External Key".<br/>                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | El método no se puede ejecutar para el volumen del sistema operativo que se está ejecutando actualmente.<br/>                                                                                       |
| <dl> <dt>**FVE \_ E \_ OS \_ NOT \_ PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | El método no se puede ejecutar si el volumen del sistema operativo que se está ejecutando actualmente no está protegido por Cifrado de unidad BitLocker o no tiene cifrado en curso.<br/> |
| <dl> <dt> **FVE \_ E VOLUME BOUND ALREADY \_ \_ \_ 2150694943**</dt> <dt>(0x8031001F)</dt> </dl> | El desbloqueo automático en el volumen se ha habilitado previamente.<br/>                                                                                                    |



 

## <a name="remarks"></a>Comentarios

Dado un protector de clave de volumen válido del tipo "Clave externa", la clave externa de 256 bits relacionada se extrae del protector y se almacena en el registro del sistema operativo que se está ejecutando actualmente, junto con el identificador del protector de clave de volumen.

Si se elimina la clave externa asociada al identificador del protector de clave de volumen, la funcionalidad para desbloquear automáticamente el volumen se deshabilita o suspende.

> [!Note]  
> Actualmente no se admiten medios extraíbles.

 

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
