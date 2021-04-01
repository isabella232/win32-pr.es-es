---
description: Permite que un volumen de datos se desbloquee automáticamente al montar el volumen.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Método EnableAutoUnlock de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910042"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Método EnableAutoUnlock de la \_ clase EncryptableVolume de Win32

El método **EnableAutoUnlock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) permite que un volumen de datos se desbloquee automáticamente al montar el volumen.

El desbloqueo automático guarda una clave externa en el sistema operativo que puede desbloquear automáticamente el volumen en el volumen del sistema operativo que se está ejecutando actualmente.

Para usar este método, el volumen del sistema operativo ya debe estar protegido por Cifrado de unidad BitLocker o debe tener cifrado en curso. Además, ya debe existir una clave externa para el volumen de datos. Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear la clave externa que puede desbloquear el volumen automáticamente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que identifica el protector de clave del tipo "clave externa" que se usa para desbloquear automáticamente el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                           | Método realizado correctamente.<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>          | El volumen está bloqueado.<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave válido del tipo "external key".<br/>                                                          |
| <dl> <dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.<br/>                                                                                       |
| <dl> <dt>**FVE \_ E \_ so \_ no \_ protegido**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | El método no se puede ejecutar si el volumen del sistema operativo que se está ejecutando actualmente no está protegido por Cifrado de unidad BitLocker o no tiene cifrado en curso.<br/> |
| <dl> <dt> **FVE \_ E \_ \_ enlazado \_ por volumen ya**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | El desbloqueo automático en el volumen se ha habilitado anteriormente.<br/>                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Dado un protector de clave de volumen válido del tipo "clave externa", se extrae la clave externa de 256 bits relacionada del protector y se almacena en el registro del sistema operativo que se está ejecutando actualmente, junto con el identificador de protector de clave de volumen.

Si se elimina la clave externa asociada con el identificador de protector de clave de volumen, la funcionalidad para desbloquear el volumen automáticamente está deshabilitada o suspendida.

> [!Note]  
> Los medios extraíbles no se admiten actualmente.

 

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

 

 
