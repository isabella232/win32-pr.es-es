---
title: WINBIO_CREDENTIAL_STATE enumeración (Winbio \_ types.h)
description: Define valores que especifican si una credencial se ha asociado a los datos biométricos de un usuario final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumeración Windows Biometric Framework API
- PWINBIO_CREDENTIAL_STATE puntero de enumeración Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868065"
---
# <a name="winbio_credential_state-enumeration"></a>Enumeración \_ CREDENTIAL STATE de WINBIO \_

Define valores que especifican si una credencial se ha asociado a los datos biométricos de un usuario final. La función [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) usa esta enumeración.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**CREDENCIALES DE WINBIO \_ \_ NO \_ ESTABLECIDAS**
</dt> <dd>

Se ha asociado una credencial al usuario final.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**CONJUNTO DE CREDENCIALES DE WINBIO \_ \_**
</dt> <dd>

No se ha asociado una credencial al usuario final.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de aplicaciones cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





