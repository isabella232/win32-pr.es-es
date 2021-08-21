---
description: 'Método UnlockWithPassphrase de la clase Win32_EncryptableVolume: usa la frase de contraseña para obtener la clave derivada.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Método UnlockWithPassphrase de Win32_EncryptableVolume clase
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
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004173"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithPassphrase de la clase EncryptableVolume de Win32 \_

El **método UnlockWithPassphrase** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, la clave derivada se usa para desbloquear la clave maestra del volumen cifrado.

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
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ EVITA LA \_ 2150695020**</dt> <dt>CONTRASEÑA (0x8031006C)</dt> </dl>          | La configuración de directiva de grupo que requiere el cumplimiento de FIPS impidió que se generara o usara la frase de contraseña. <br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH 2150695040**</dt> <dt>(0x80310080)</dt> </dl> | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.<br/>                              |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO SIMPLE \_ 2150695041**</dt> <dt>(0x80310081)</dt> </dl>     | La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la directiva de grupo.<br/>             |
| <dl> <dt>**FVE \_ E \_ ERROR \_ DE AUTENTICACIÓN**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>              | El volumen no se puede desbloquear con la información proporcionada. <br/>                                                  |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | El protector de clave proporcionado no existe en el volumen. Debe escribir otro protector de clave.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




