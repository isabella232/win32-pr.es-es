---
description: Comienza el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método Decrypt de la Win32_EncryptableVolume (Infocard.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e9018cfab8bea6c149c4771a54dbe55a62afafd447f4db2e162aa76d183c28ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004633"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Método Decrypt de la clase EncryptableVolume de Win32 \_

El **método Decrypt** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) comienza el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.

Cuando el descifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Cuando el cifrado está en pausa o en curso, este método revierte el cifrado y comienza el descifrado. Una vez completado el descifrado, todos los protectores de clave de este volumen se quitan del sistema y el volumen se convierte en un sistema de archivos NTFS estándar.

> [!Note]  
> Si el disco está cifrado por hardware, el método **Decrypt** establece el estado de la banda en "siempre desbloqueado", quita todos los metadatos asociados y pone a cero el identificador de seguridad de la unidad.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Este método devuelve inmediatamente. Si el volumen ya está completamente descifrado y no existe ningún otro error, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                       | Método realizado correctamente.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>      | El volumen está bloqueado.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ AUTOUNLOCK \_ ENABLED**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Este volumen no se puede descifrar porque las claves usadas para desbloquear automáticamente volúmenes de datos están disponibles. <br/> Use [**ClearAllAutoUnlockKeys para**](clearallautounlockkeys-win32-encryptablevolume.md) quitar estas claves.<br/> |



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Llamar al **método Decrypt** deja los datos sin protección.

Si el estado de protección del volumen es 1 (PROTECTION ON) antes de usar este método, la finalización correcta de este método cambia el estado de protección a 0 (PROTECTION OFF), ya que por definición un volumen parcialmente cifrado no está protegido.

## <a name="remarks"></a>Comentarios

Si el volumen aún no está descifrado por completo, la ejecución de **Decrypt** hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el descifrado está en curso y muestra el porcentaje del volumen que permanece cifrado.

Si el estado de protección del volumen es "on" antes de ejecutar este método, la ejecución de este método cambia el estado de protección a "off", ya que por definición un volumen parcialmente cifrado no está protegido.

Si este método se ejecuta en el volumen del sistema operativo que se está ejecutando actualmente y este volumen de sistema operativo se usa para desbloquear automáticamente los volúmenes de datos (consulte el método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), primero debe llamar al método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| Header<br/>                   | <dl> <dt>Infocard.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
