---
description: 'Método ProtectKeyWithPassphrase de la clase Win32_EncryptableVolume: usa la frase de contraseña para obtener la clave derivada.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c0d87eb21ea505b13ce3aacfe8be6ff1fa9d266ba2a781d6b8e6fc4d77dac10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004363"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithPassphrase de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithPassphrase** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, la clave derivada se usa para proteger la clave maestra del volumen cifrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se usa un valor en blanco.

</dd> <dt>

*Frase de contraseña* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la frase de contraseña.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica de forma única el protector de clave creado.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                        | Descripción                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Método realizado correctamente.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ NO SE PERMITE EN EL MODO \_ \_ \_ \_ SEGURO**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Cifrado de unidad BitLocker solo se puede usar con fines de recuperación cuando se usa en Caja fuerte modo.<br/>                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ NOT \_ ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | La directiva de grupo no permite la creación de una frase de contraseña.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ EVITA LA \_ 2150695020**</dt> <dt>CONTRASEÑA (0x8031006C)</dt> </dl>           | La configuración de directiva de grupo que requiere el cumplimiento de FIPS impidió que se generara o usara la frase de contraseña.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH 2150695040**</dt> <dt>(0x80310080)</dt> </dl>  | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.<br/>                             |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO SIMPLE \_ 2150695041**</dt> <dt>(0x80310081)</dt> </dl>      | La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la directiva de grupo.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | El volumen ya está bloqueado por Cifrado de unidad BitLocker. Debe desbloquear la unidad desde Panel de control.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Otro subproceso actualizó el bloque de control para el volumen cifrado.<br/>                                     |
| <dl> <dt>**FVE \_ E \_ KEY PROTECTOR NOT \_ \_ \_ SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | El protector de clave no es compatible con la versión de Cifrado de unidad BitLocker actualmente en el volumen.<br/>      |
| <dl> <dt>**FVE \_ E \_ NO SE PERMITE \_ LA \_ \_ \_**</dt> FRASE DE CONTRASEÑA DEL VOLUMEN <dt>2150695021 SISTEMA OPERATIVO (0x8031006D)</dt> </dl> | La frase de contraseña no se puede agregar al volumen del sistema operativo. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | El protector de clave proporcionado ya existe en este volumen.<br/>                                                     |



 

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

 

 




