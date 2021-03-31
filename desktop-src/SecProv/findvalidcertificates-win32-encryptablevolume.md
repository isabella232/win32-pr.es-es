---
description: Enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Método FindValidCertificates de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361050"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Método FindValidCertificates de la \_ clase EncryptableVolume de Win32

El método **FindValidCertificates** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales. La lista devuelta solo contiene certificados con un [*identificador de objeto*](../secgloss/o-gly.md) (OID) válido. El OID puede ser el valor predeterminado, o bien se puede especificar en el directiva de grupo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CertificateThumbprint* \[ enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Matriz de cadenas que contiene la lista de certificados válidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                           | Método realizado correctamente.<br/>                |
| <dl> <dt>**FVE \_ E \_ no \_ válido \_ OID de BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> </dl> | El OID de BitLocker disponible no es válido.<br/> |



 

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

 

 
