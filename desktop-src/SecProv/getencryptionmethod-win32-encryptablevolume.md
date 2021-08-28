---
description: Indica el algoritmo de cifrado y el tamaño de clave usados en el volumen.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Método GetEncryptionMethod de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: f9f4a2ad20af7c5ee3ba3afd8e2d9e56d0720b38d7afc2b01042e440cc85bf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892453"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Método GetEncryptionMethod de la clase EncryptableVolume de Win32 \_

El **método GetEncryptionMethod** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el algoritmo de cifrado y el tamaño de clave usados en el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncryptionMethod* \[ out\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que especifica el algoritmo de cifrado y el tamaño de clave usados en el volumen.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Ninguno**</dt> <dt>0</dt> </dl>                                | El volumen no está cifrado.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ CON \_ DIFUSOR**</dt> <dt>1</dt> </dl> | El volumen se ha cifrado total o parcialmente con el algoritmo Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave AES de 128 bits. Este método ya no está disponible en dispositivos que ejecutan Windows 8.1 o superior.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ CON \_ DIFUSOR**</dt> <dt>2</dt> </dl> | El volumen se ha cifrado total o parcialmente con el algoritmo Estándar de cifrado avanzado (AES) mejorado con una capa de difusor, con un tamaño de clave AES de 256 bits. Este método ya no está disponible en dispositivos que ejecutan Windows 8.1 o superior.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | El volumen se ha cifrado total o parcialmente con el algoritmo Estándar de cifrado avanzado (AES), con un tamaño de clave AES de 128 bits.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | El volumen se ha cifrado total o parcialmente con el algoritmo Estándar de cifrado avanzado (AES), con un tamaño de clave AES de 256 bits.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**HARDWARE \_ CIFRADO**</dt> <dt>5</dt> </dl>         | El volumen se ha cifrado total o parcialmente mediante las funcionalidades de hardware de la unidad.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave AES de 128 bits. Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | El volumen se ha cifrado total o parcialmente con XTS mediante el Estándar de cifrado avanzado (AES) y un tamaño de clave AES de 256 bits. Este método solo está disponible en dispositivos que ejecutan Windows 10, versión 1511 o posterior.<br/>                          |
| <dl> <dt>(uint32)–1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> El volumen se ha cifrado total o parcialmente con un algoritmo y un tamaño de clave desconocidos.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ out\]
</dt> <dd>

Tipo: **cadena**

El algoritmo de cifrado se configura en la unidad de cifrado automático. Una cadena null significa que BitLocker usa cifrado de software o no se notifica ningún método de cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
