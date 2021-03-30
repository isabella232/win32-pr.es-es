---
description: Indica el estado del cifrado o descifrado en el volumen.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Método GetConversionStatus de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907811"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetConversionStatus de la \_ clase EncryptableVolume de Win32

El método **GetConversionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el estado del cifrado o descifrado en el volumen.

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

*ConversionStatus* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Estado de cifrado o descifrado de volumen. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | En el caso de una unidad de disco duro estándar (HDD), el volumen se descifra por completo.<br/> En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen se desbloquea de forma perpetua.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | En el caso de una unidad de disco duro estándar (HDD), el volumen está totalmente cifrado.<br/> En el caso de una unidad de disco duro cifrada de hardware (EHDD), el volumen no se desbloquea de forma perpetua.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**Durante**</dt> <dt>2</dt> </dl> | El volumen está parcialmente cifrado.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | El volumen está parcialmente cifrado.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | El volumen se ha pausado durante el progreso del cifrado. El volumen está parcialmente cifrado.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | El volumen se ha pausado durante el progreso del descifrado. El volumen está parcialmente cifrado.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Porcentaje del volumen cifrado. Es un entero comprendido entre 0 y 100, ambos inclusive.

Debido al redondeo de números, un porcentaje de cifrado de 0 o 100 no indica necesariamente que el disco se haya descifrado o totalmente cifrado. Use siempre *ConversionStatus* para determinar si el disco se ha descifrado completamente o está totalmente cifrado.

</dd> <dt>

*EncryptionFlags* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Marcas que describen el comportamiento de cifrado.

Combinación de 32 bits con los siguientes bits definidos actualmente.



| Value                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Realice el cifrado de volumen en el modo de cifrado de solo datos al iniciar un nuevo proceso de cifrado. Si el cifrado se ha pausado o detenido, la llamada al método de [**cifrado**](encrypt-win32-encryptablevolume.md) reanuda de forma eficaz la conversión y se omite el valor de este bit. Este bit solo tiene efecto cuando los métodos **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) inician el cifrado del estado de pausa del estado descifrado, el descifrado en el estado de progreso o el descifrado. Si este bit es cero, lo que significa que no se establece, cuando se inicia un nuevo proceso de cifrado, se realizará la conversión de modo completo.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Realice un borrado a petición del espacio libre del volumen. Solo se permite llamar al método [**Encrypt**](encrypt-win32-encryptablevolume.md) con este conjunto de bits cuando el volumen no se está convirtiendo o borrando actualmente y se encuentra en un estado "cifrado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Realizar la operación solicitada sincrónicamente. La llamada se bloqueará hasta que la operación solicitada se haya completado o se haya interrumpido. Esta marca solo se admite con el método [**Encrypt**](encrypt-win32-encryptablevolume.md) . Esta marca se puede especificar cuando se llama a **Encrypt** para reanudar el cifrado o la eliminación interrumpida o interrumpida, o cuando el cifrado o la eliminación están en curso. Esto permite que el autor de la llamada reanude la espera de forma sincrónica hasta que el proceso se complete o se interrumpa.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Estado de limpieza de espacio disponible. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                               | Significado                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | No se ha borrado el espacio disponible.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | Se ha borrado el espacio disponible.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | La eliminación de espacio disponible está actualmente en curso.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | Se pausó el barrido de espacio disponible.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Un valor de 0 a 100 que especifica el porcentaje de espacio libre que se ha borrado.

</dd> <dt>

*PrecisionFactor* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Un valor de 0 a 4 que especifica el nivel de precisión

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Observaciones

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

 

 
