---
description: Enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Método FindValidCertificates de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: da642ff24fa01d27c74a30af7de6c7f91e33a712a28c47644a7044f43c40d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892443"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Método FindValidCertificates de la clase EncryptableVolume de Win32 \_

El **método FindValidCertificates** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera todos los certificados del sistema que coinciden con los criterios indicados y devuelve una lista de huellas digitales. La lista devuelta solo contiene certificados con un identificador de [*objeto*](../secgloss/o-gly.md) (OID) válido. El OID puede ser el valor predeterminado o puede especificarse en el directiva de grupo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CertificateThumbprint* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz de cadenas que contiene la lista de certificados válidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                           | Método realizado correctamente.<br/>                |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID de BITLOCKER no**</dt> <dt>válido 2150695022 (0x8031006E)</dt> </dl> | El OID de BitLocker disponible no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
