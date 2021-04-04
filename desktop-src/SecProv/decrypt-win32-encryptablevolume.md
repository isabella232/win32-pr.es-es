---
description: Inicia el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Método de descifrado de la clase Win32_EncryptableVolume (InfoCard. h)
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
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910054"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Método de descifrado de la \_ clase EncryptableVolume de Win32

El método de **descifrado** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inicia el descifrado de un volumen totalmente cifrado o reanuda el descifrado de un volumen parcialmente cifrado.

Cuando el descifrado está en pausa o en curso, este método se comporta igual que [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Cuando el cifrado está en pausa o en curso, este método revierte el cifrado y comienza el descifrado. Una vez completado el descifrado, todos los protectores de clave de este volumen se quitan del sistema y el volumen se convierte en un sistema de archivos NTFS estándar.

> [!Note]  
> Si el disco está cifrado por hardware, el método de **descifrado** establece el estado de la banda en "siempre desbloqueado", quita todos los metadatos asociados y pone a cero el ID. de seguridad de la unidad.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Este método vuelve inmediatamente. Si el volumen ya está completamente descifrado y no existe ningún otro error, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                       | Descripción                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                       | Método realizado correctamente.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | El volumen está bloqueado.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ DESbloqueo automático \_ habilitado**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Este volumen no se puede descifrar porque están disponibles las claves usadas para desbloquear automáticamente los volúmenes de datos. <br/> Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para quitar estas claves.<br/> |



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

La llamada al método **Decrypt** deja los datos desprotegidos.

Si el estado de protección del volumen es 1 (protección activada) antes de que se use este método, la finalización correcta de este método cambia el estado de protección a 0 (protección desactivada), ya que, por definición, un volumen parcialmente cifrado no está protegido.

## <a name="remarks"></a>Observaciones

Si el volumen no se ha descifrado por completo, al ejecutar **descifrado** , [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indica que el descifrado es Progress y muestra el porcentaje del volumen que permanece cifrado.

Si el estado de protección del volumen es "activado" antes de que se ejecute este método, la ejecución de este método cambia el estado de protección a "desactivado", ya que, por definición, un volumen parcialmente cifrado no está protegido.

Si este método se ejecuta en el volumen del sistema operativo que se está ejecutando actualmente y se usa este volumen del sistema operativo para desbloquear automáticamente los volúmenes de datos (consulte el método [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), primero debe llamar al método [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]<br/>                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>InfoCard. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
