---
description: Indica si el volumen y su clave de cifrado están protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809283"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetProtectionStatus de la \_ clase EncryptableVolume de Win32

El método **GetProtectionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen y su clave de cifrado (si existen) están protegidos.

La protección está desactivada si un volumen no está cifrado o parcialmente cifrado, o si la clave de cifrado del volumen está disponible en el disco duro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtectionStatus* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Especifica si el volumen y la clave de cifrado (si existen) están protegidos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <dt><strong>Desprotegido</strong></dt> <dt>0</dt> </dl></td>
<td>PROTECCIÓN DESACTIVADA<br/> Para una unidad de disco duro estándar:<br/> El volumen está sin cifrar, parcialmente cifrado o la clave de cifrado del volumen está disponible en el disco duro. La clave de cifrado está disponible en el disco duro sin cifrado si se han deshabilitado los protectores de clave mediante el método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o si no se ha especificado ningún protector de clave mediante los métodos siguientes:
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
<br/> Para un EHDD:<br/> La banda del volumen se desbloquea perpetuamente, no tiene administrador de claves o está administrada por un administrador de claves de terceros.<br/> Esto también puede significar que la banda está administrada por BitLocker, pero se ha llamado al método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> y la unidad está suspendida.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Protegido</strong></dt> <dt>1</dt> </dl></td>
<td>PROTECCIÓN ACTIVADA<br/> Para una unidad de disco duro estándar:<br/> El volumen está totalmente cifrado y la clave de cifrado del volumen no está disponible en el disco duro.<br/> Para un EHDD:<br/> BitLocker es el administrador de claves de la banda. La unidad puede estar bloqueada o desbloqueada, pero no se puede desbloquear perpetuamente.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Desconocido</strong></dt> <dt>2</dt> </dl></td>
<td>No se puede determinar el estado de protección del volumen. Esto puede deberse a que el volumen está en estado bloqueado.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise y Windows Server 2008:</strong> Este valor no se admite. Este valor se admite a partir de Windows 7 y Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo se puede cifrar un volumen si se llama a [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) en primer lugar o se usa uno de los métodos siguientes:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Por lo tanto, si el disco está cifrado y *ProtectionStatus* devuelve cero (protección desactivada), se deshabilitan las claves.

Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) para enumerar los protectores de clave especificados para proteger la clave de cifrado del volumen. Si existen protectores de clave pero la protección es cero (protección desactivada), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para activar la protección del volumen.

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

 

 
