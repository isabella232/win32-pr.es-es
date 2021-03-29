---
description: Reanuda el cifrado o descifrado de un volumen.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Método ResumeConversion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809277"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Método ResumeConversion de la \_ clase EncryptableVolume de Win32

El método **ResumeConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) reanuda el cifrado o descifrado de un volumen.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función solo puede reanudar una operación de eliminación. Para obtener más información, vea [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Si este método se usa en un volumen totalmente cifrado o completamente descifrado, o si el cifrado o descifrado ya está en curso en el volumen, se devuelve 0 si no se produce ningún otro error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Observaciones

Si este método se usa en un volumen con cifrado o descifrado en pausa, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en curso.

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

 

 
