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
ms.openlocfilehash: e947cb5fadefa6703ab4515ddd8d2a9daf1e7439e514e75c64d3b1e6e885aa0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892068"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorCertificate de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorCertificate** de la clase [**\_ EncryptableVolume**](win32-encryptablevolume.md) de [](../secgloss/c-gly.md) Win32 recupera la clave pública y la huella digital del certificado para un protector de clave pública. [](../secgloss/p-gly.md)

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



| Valor                                                                        | Significado                                  |
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
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Esta unidad está bloqueada por Cifrado de unidad BitLocker. Debe desbloquear este volumen desde Panel de control. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE \_ \_ \_ REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | directiva de grupo requiere el uso de un certificado de usuario, como una tarjeta inteligente.<br/>                           |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de escritorio Ultimate \[\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
