---
description: Usa la frase de contraseña para obtener la clave derivada.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668468"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithPassphrase de la \_ clase EncryptableVolume de Win32

El método **UnlockWithPassphrase** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, se usa la clave derivada para desbloquear la clave maestra del volumen cifrado.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Frase de contraseña* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la frase de contraseña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                       | Descripción                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                       | Método realizado correctamente.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ evita la \_ frase de contraseña**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | La configuración de directiva de grupo que requiere el cumplimiento de FIPS impidió la generación o el uso de la frase de contraseña. <br/> |
| <dl> <dt>**FVE \_ La longitud de la frase de contraseña de la \_ Directiva E \_ no es \_ \_**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.<br/>                              |
| <dl> <dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ demasiado \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la Directiva de grupo.<br/>             |
| <dl> <dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | No se puede desbloquear el volumen con la información proporcionada. <br/>                                                  |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | El protector de clave proporcionado no existe en el volumen. Debe especificar otro protector de clave.<br/>                 |



 

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

 

 




