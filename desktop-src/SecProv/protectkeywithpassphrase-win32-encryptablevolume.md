---
description: Usa la frase de contraseña para obtener la clave derivada.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Método ProtectKeyWithPassphrase de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666386"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithPassphrase de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithPassphrase** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la frase de contraseña para obtener la clave derivada. Una vez calculada la clave derivada, la clave derivada se usa para proteger la clave maestra del volumen cifrado.

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

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se utiliza un valor en blanco.

</dd> <dt>

*Frase de contraseña* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la frase de contraseña.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena que identifica de forma única el protector de clave creado.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                        | Descripción                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                        | Método realizado correctamente.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ no \_ permitido \_ en \_ \_ modo seguro**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Cifrado de unidad BitLocker solo se puede usar con fines de recuperación cuando se usa en modo seguro.<br/>                     |
| <dl> <dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ no \_ permitida**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | La Directiva de grupo no permite la creación de una frase de contraseña.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ evita la \_ frase de contraseña**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | La configuración de directiva de grupo que requiere el cumplimiento de FIPS impidió la generación o el uso de la frase de contraseña.<br/> |
| <dl> <dt>**FVE \_ La longitud de la frase de contraseña de la \_ Directiva E \_ no es \_ \_**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | La frase de contraseña proporcionada no cumple los requisitos de longitud mínima o máxima.<br/>                             |
| <dl> <dt>**FVE \_ Frase de contraseña de la Directiva de E \_ \_ \_ demasiado \_ simple**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | La frase de contraseña no cumple los requisitos de complejidad establecidos por el administrador en la Directiva de grupo.<br/>            |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | El volumen ya está bloqueado por Cifrado de unidad BitLocker. Debe desbloquear la unidad desde el panel de control.<br/>     |
| <dl> <dt>**FVE \_ E \_ SUPERpuesto ( \_ actualización**</dt> <dt>2150694948) (0x80310024)</dt> </dl>                   | Otro subproceso actualizó el bloque de control para el volumen cifrado.<br/>                                     |
| <dl> <dt>**FVE \_ \_No se \_ \_ \_ admite el PROTECTOR de clave E**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | El protector de clave no es compatible con la versión de Cifrado de unidad BitLocker actualmente en el volumen.<br/>      |
| <dl> <dt>**FVE \_ \_No se \_ \_ \_ \_ permite la frase de contraseña del volumen del sistema operativo**</dt> <dt>2150695021 (0x8031006D)</dt> </dl> | La frase de contraseña no se puede Agregar al volumen del sistema operativo. <br/>                                               |
| <dl> <dt>**FVE \_ El \_ protector E \_ existe**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | El protector de clave proporcionado ya existe en este volumen.<br/>                                                     |



 

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

 

 




