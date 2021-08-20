---
description: Pausa el cifrado o descifrado de un volumen.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Método PauseConversion de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7612f7f587d13bb1dbe5fc96d29117d126b3a7166e0172abe98a0777d815effa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004453"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Método PauseConversion de la clase EncryptableVolume de Win32 \_

El **método PauseConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) pausa el cifrado o descifrado de un volumen.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función puede pausar una operación de limpieza, pero no puede pausar el cifrado basado en hardware.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si este método se usa en un volumen totalmente cifrado o totalmente descifrado, o si el cifrado o descifrado ya está en pausa en el volumen, se devuelve 0 suponiendo que no se produzcan otros errores.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentarios

Si este método se usa en un volumen con cifrado y descifrado en curso, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en pausa.

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

 

 
