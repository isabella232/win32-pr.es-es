---
description: Reanuda el cifrado o descifrado de un volumen.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Método ResumeConversion de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: e1b3908f77b72f7f9a5ca0583193784ba054a50ab59aa63dad1c13b9f03317e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992675"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Método ResumeConversion de la clase EncryptableVolume de Win32 \_

El **método ResumeConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) reanuda el cifrado o descifrado de un volumen.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función solo puede reanudar una operación de limpieza. Para obtener más información, [**vea PauseConversion**](pauseconversion-win32-encryptablevolume.md).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si este método se usa en un volumen totalmente cifrado o totalmente descifrado, o si el cifrado o descifrado ya está en curso en el volumen, se devuelve 0 suponiendo que no se produzcan otros errores.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentarios

Si este método se usa en un volumen con cifrado o descifrado en pausa, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en curso.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
