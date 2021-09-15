---
description: Recupera la clave pública y la huella digital del certificado para un protector de clave pública.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Método GetKeyProtectorCertificate de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270807"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorCertificate de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorCertificate** de la clase [](../secgloss/p-gly.md) [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la clave pública y la huella digital del certificado para un protector de clave pública. [](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*PublicKey* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que especifica la clave pública.

</dd> <dt>

*CertThumbprint* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la huella digital del certificado.

</dd> <dt>

*CertType* \[ out\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que especifica el tipo del protector de clave. Este entero se usa para diferenciar entre el agente de recuperación de datos (DRA) y los certificados de usuario.



| Value                                                                        | Significado                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | El certificado es un DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | El certificado no es un DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                       | Descripción                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Método realizado correctamente.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | El protector de clave especificado no es un protector de clave. Debe escribir otro protector de clave.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>                      | Esta unidad está bloqueada por Cifrado de unidad BitLocker. Debe desbloquear este volumen desde Panel de control. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE \_ \_ \_ REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | directiva de grupo requiere el uso de un certificado de usuario, como una tarjeta inteligente.<br/>                           |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de escritorio Ultimate \[\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
