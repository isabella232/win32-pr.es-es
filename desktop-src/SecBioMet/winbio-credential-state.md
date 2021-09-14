---
title: WINBIO_CREDENTIAL_STATE enumeración (Winbio \_ types.h)
description: Define valores que especifican si una credencial se ha asociado a los datos biométricos de un usuario final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumeración Windows BIOMETRIC Framework API
- PWINBIO_CREDENTIAL_STATE puntero de enumeración Windows API de marco biométrico
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
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160771"
---
# <a name="winbio_credential_state-enumeration"></a>Enumeración \_ CREDENTIAL STATE de WINBIO \_

Define valores que especifican si una credencial se ha asociado a los datos biométricos de un usuario final. La función [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) usa esta enumeración.

## <a name="syntax"></a>Sintaxis


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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de aplicaciones cliente](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





