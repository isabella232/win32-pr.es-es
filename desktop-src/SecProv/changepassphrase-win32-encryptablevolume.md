---
description: Usa la nueva frase de contraseña para obtener una nueva clave derivada.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Método ChangePassphrase de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688169"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ChangePassphrase de la \_ clase EncryptableVolume de Win32

El método **ChangePassphrase** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la nueva frase de contraseña para obtener una nueva clave derivada. Una vez calculada la clave derivada, se usa la nueva clave derivada para proteger la clave maestra del volumen cifrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*NewPassphrase* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena actualizada que especifica la frase de contraseña.

</dd> <dt>

*NewProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                       | Descripción                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                       | Método realizado correctamente.<br/>                                                                                  |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | El volumen ya está bloqueado por Cifrado de unidad BitLocker. Debe desbloquear la unidad desde el panel de control.<br/>   |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                           |
| <dl> <dt>**FVE \_ E \_ SUPERpuesto ( \_ actualización**</dt> <dt>2150694948) (0x80310024)</dt> </dl>                  | Otro subproceso actualizó el bloque de control para el volumen cifrado.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido </dl>            | El protector de clave especificado no es del tipo correcto. <br/>                                                    |
| <dl> <dt>**FVE \_ La longitud de la frase de contraseña de la \_ Directiva E \_ no es \_ \_**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima. <br/>                  |
| <dl> <dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ demasiado \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La frase de contraseña actualizada no cumple los requisitos de complejidad establecidos por el administrador en la Directiva de grupo. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




