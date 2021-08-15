---
description: Indica si el volumen y su clave de cifrado están protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 44fde17ee8e7d4d7bacd5c63743af045f89e16f840c193df8d883a5c80111659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891885"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetProtectionStatus de la clase EncryptableVolume de Win32 \_

El **método GetProtectionStatus** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen y su clave de cifrado (si existe) están protegidos.

La protección está desactivada si un volumen está sin cifrar o parcialmente cifrado, o si la clave de cifrado del volumen está disponible de forma transparente en el disco duro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtectionStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Especifica si el volumen y la clave de cifrado (si existe) están protegidos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <dt><strong>Sin protección</strong></dt> <dt>0</dt> </dl></td>
<td>PROTECCIÓN DESACTIVADA<br/> Para un HDD estándar:<br/> El volumen está sin cifrar, parcialmente cifrado o la clave de cifrado del volumen está disponible sin cifrar en el disco duro. La clave de cifrado está disponible sin cifrar en el disco duro si los protectores de clave se han deshabilitado mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o si no se ha especificado ningún protector de clave mediante los métodos siguientes:
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/> Para un EHDD:<br/> La banda del volumen está desbloqueada permanentemente, no tiene ningún administrador de claves o está administrada por un administrador de claves de terceros.<br/> Esto también puede significar que BitLocker administra la banda, pero se ha llamado al método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> y se suspende la unidad.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Protegido</strong></dt> <dt>1</dt> </dl></td>
<td>PROTECCIÓN EN<br/> Para un HDD estándar:<br/> El volumen está totalmente cifrado y la clave de cifrado del volumen no está disponible en el disco duro.<br/> Para un EHDD:<br/> BitLocker es el administrador de claves de la banda. La unidad se puede bloquear o desbloquear, pero no se puede desbloquear permanentemente.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Desconocido</strong></dt> <dt>2</dt> </dl></td>
<td>No se puede determinar el estado de protección del volumen. Esto puede deberse a que el volumen está en un estado bloqueado.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise y Windows Server 2008:</strong> Este valor no se admite. Este valor se admite a partir de Windows 7 y Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo puede cifrar un volumen si llama primero a [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) o usa uno de los métodos siguientes:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Por lo tanto, si el disco está cifrado y *ProtectionStatus* devuelve cero (PROTECTION OFF), las claves se deshabilitan.

Use [**GetKeyProtectors para**](getkeyprotectors-win32-encryptablevolume.md) enumerar los protectores de clave que se han especificado para proteger la clave de cifrado del volumen. Si existen protectores de clave pero la protección es cero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para activar la protección por volumen.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
