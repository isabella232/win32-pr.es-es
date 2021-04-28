---
description: 'Método UnlockWithPassphrase de la clase Win32_EncryptableVolume : usa la frase de contraseña para obtener la clave derivada.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116463"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithPassphrase de la clase EncryptableVolume de Win32 \_

El **método UnlockWithPassphrase** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, se usa la clave derivada para desbloquear la clave maestra del volumen cifrado.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Frase de contraseña* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la frase de contraseña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                       | Descripción                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Método realizado correctamente.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ NO \_ ACTIVADO**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ EVITA LA FRASE \_ DE CONTRASEÑA**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | La configuración de directiva de grupo que requiere el cumplimiento de FIPS impedía que la frase de contraseña se generara o usara. <br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.<br/>                              |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la directiva de grupo.<br/>             |
| <dl> <dt>**FVE \_ E \_ ERROR \_ DE AUTENTICACIÓN**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | El volumen no se puede desbloquear con la información proporcionada. <br/>                                                  |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | El protector de clave proporcionado no existe en el volumen. Debe escribir otro protector de clave.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




