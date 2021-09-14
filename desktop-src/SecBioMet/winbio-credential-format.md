---
title: WINBIO_CREDENTIAL_FORMAT enumeración (Winbio \_ types.h)
description: Define las marcas que se pueden usar para especificar el formato de credenciales del usuario final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumeración Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071156"
---
# <a name="winbio_credential_format-enumeration"></a>Enumeración WINBIO \_ CREDENTIAL \_ FORMAT

Define las marcas que se pueden usar para especificar el formato de credenciales del usuario final. La función [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) usa esta enumeración.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**CONTRASEÑA GENÉRICA DE WINBIO \_ \_**
</dt> <dd>

La contraseña está en un formato genérico.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**CONTRASEÑA DE WINBIO \_ \_ EMPAQUETADA**
</dt> <dd>

La contraseña está en un formato comprimido.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ PASSWORD \_ PROTECTED**
</dt> <dd>

La credencial de contraseña se ha ajustado [**con CredProtect.**](/windows/desktop/api/wincred/nf-wincred-credprotecta)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de aplicaciones cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

