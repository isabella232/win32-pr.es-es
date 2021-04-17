---
description: Indica el algoritmo de cifrado y el tamaño de la clave usados en el volumen.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Método GetEncryptionMethod de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688168"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Método GetEncryptionMethod de la \_ clase EncryptableVolume de Win32

El método **GetEncryptionMethod** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el algoritmo de cifrado y el tamaño de clave usados en el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncryptionMethod* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Entero sin signo que especifica el algoritmo de cifrado y el tamaño de clave usados en el volumen.



| Value                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Ninguno**</dt> <dt>0</dt> </dl>                                | El volumen no está cifrado.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ con \_ difusor**</dt> <dt>1</dt> </dl> | El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave de AES de 128 bits. Este método ya no está disponible en los dispositivos que ejecutan Windows 8.1 o posterior.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ con \_ difusor**</dt> <dt>2</dt> </dl> | El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave de AES de 256 bits. Este método ya no está disponible en los dispositivos que ejecutan Windows 8.1 o posterior.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) con un tamaño de clave AES de 128 bits.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | El volumen se ha cifrado total o parcialmente con el algoritmo de Estándar de cifrado avanzado (AES) con un tamaño de clave AES de 256 bits.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**Hardware \_ de CIFRAdo**</dt> <dt>5</dt> </dl>         | El volumen se ha cifrado total o parcialmente con las capacidades de hardware de la unidad.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave de AES de 128 bits. Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave de AES de 256 bits. Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.<br/>                          |
| <dl> <dt>(UInt32) – 1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> El volumen se ha cifrado total o parcialmente con un algoritmo y un tamaño de clave desconocidos.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ enuncia\]
</dt> <dd>

Tipo: **String**

El algoritmo de cifrado se configura en la unidad de cifrado automático. Una cadena nula significa que BitLocker usa el cifrado de software o no se indica ningún método de cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

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

 

 
