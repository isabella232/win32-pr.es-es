---
description: Indica el estado del cifrado o descifrado en el volumen.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004492"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetConversionStatus de la clase EncryptableVolume de Win32 \_

El **método GetConversionStatus** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el estado del cifrado o descifrado en el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ConversionStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Estado de cifrado o descifrado del volumen. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | En el caso de una unidad de disco duro (HDD) estándar, el volumen se descifra completamente.<br/> En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen se desbloquea permanentemente.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | En el caso de una unidad de disco duro (HDD) estándar, el volumen está totalmente cifrado.<br/> En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen no se desbloquea permanentemente.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | El volumen está parcialmente cifrado.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | El volumen está parcialmente cifrado.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | El volumen se ha pausado durante el progreso del cifrado. El volumen está parcialmente cifrado.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | El volumen se ha pausado durante el progreso del descifrado. El volumen está parcialmente cifrado.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ out\]
</dt> <dd>

Tipo: **uint32**

Porcentaje del volumen cifrado. Se trata de un entero comprendido entre 0 y 100, ambos incluidos.

Debido al redondeo de números, un porcentaje de cifrado de 0 o 100 no indica necesariamente que el disco está completamente descifrado o totalmente cifrado. Use siempre *ConversionStatus para* determinar si el disco está de hecho totalmente descifrado o totalmente cifrado.

</dd> <dt>

*EncryptionFlags* \[ out\]
</dt> <dd>

Tipo: **uint32**

Marcas que describen el comportamiento de cifrado.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Value                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realizar el cifrado de volumen en modo de cifrado solo de datos al iniciar el nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, al llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) se reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado desde el estado completamente descifrado, descifrado en estado en curso o estado en pausa de descifrado. Si este bit es cero, lo que significa que no está establecido, al iniciar el nuevo proceso de cifrado, se realizará la conversión en modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice el borrado a petición del espacio libre del volumen. Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o limpiando actualmente y está en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Realice la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el [**método Encrypt.**](encrypt-win32-encryptablevolume.md) Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado detenido o interrumpido o cuando el cifrado o el borrar están en curso. Esto permite que el autor de la llamada se reanude sincrónicamente esperando hasta que se complete o interrumpa el proceso.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Estado de limpieza del espacio libre. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                               | Significado                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | No se ha borrado el espacio libre.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | Se ha borrado el espacio libre.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | El limpieza de espacio libre está actualmente en curso.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | Se ha pausado el limpieza de espacio libre.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ out\]
</dt> <dd>

Tipo: **uint32**

Valor de 0 a 100 que especifica el porcentaje de espacio libre que se ha borrado.

</dd> <dt>

*PrecisionFactor* \[ En\]
</dt> <dd>

Tipo: **uint32**

Valor de 0 a 4 que especifica el nivel de precisión

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, solo Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
