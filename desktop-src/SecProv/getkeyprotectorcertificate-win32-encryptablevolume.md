---
description: Recupera la clave pública y la huella digital del certificado para un protector de clave pública.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Método GetKeyProtectorCertificate de la clase Win32_EncryptableVolume
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688157"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorCertificate de la \_ clase EncryptableVolume de Win32

El método **GetKeyProtectorCertificate** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la [*clave pública*](../secgloss/p-gly.md) y la huella digital del [*certificado*](../secgloss/c-gly.md) para un protector de clave pública.

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

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*PublicKey* \[ enuncia\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que especifica la clave pública.

</dd> <dt>

*CertThumbprint* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la huella digital del certificado.

</dd> <dt>

*CertType* \[ enuncia\]
</dt> <dd>

Tipo: **UInt32**

Entero sin signo que especifica el tipo del protector de clave. Este entero se usa para diferenciar entre el agente de recuperación de datos (DRA) y los certificados de usuario.



| Value                                                                        | Significado                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | El certificado es un DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | El certificado no es un DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                       | Descripción                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                       | Método realizado correctamente.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | El protector de clave especificado no es un protector de clave. Debe especificar otro protector de clave.<br/>            |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Esta unidad está bloqueada por Cifrado de unidad BitLocker. Debe desbloquear este volumen en el panel de control. <br/> |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ Certificado de usuario de directiva de E \_ \_ \_ \_ requerido**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Directiva de grupo requiere el uso de un certificado de usuario, como una tarjeta inteligente.<br/>                           |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
