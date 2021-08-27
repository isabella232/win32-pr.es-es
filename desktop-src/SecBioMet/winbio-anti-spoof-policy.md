---
title: WINBIO_ANTI_SPOOF_POLICY estructura (Winbio \_ types.h)
description: Representa la directiva de antispoofing para un usuario.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY estructura Windows API de Marco biométrico
- PWINBIO_ANTI_SPOOF_POLICY puntero de estructura Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ade20749b105cc3c7f8a92e0904aff1cea860f9175c8b3c6adb113f273f0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073255"
---
# <a name="winbio_anti_spoof_policy-structure"></a>Estructura DE \_ DIRECTIVAS \_ ANTI SPOOF \_ de WINBIO

Representa la directiva de antispoofing para un usuario.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Acción**
</dt> <dd>

Tipo de acción que se debe realizar para la directiva de antispoofing.

</dd> <dt>

**Origen**
</dt> <dd>

Origen de la directiva de antispoofing.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACCIÓN DE \_ DIRECTIVA \_ ANTI SUPLANTACIÓN \_ DE SEGURIDAD DE \_ WINBIO**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**ORIGEN DE \_ LA DIRECTIVA \_ WINBIO**](winbio-policy-source.md)
</dt> <dt>

[**RESULTADO \_ DE WINBIO ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





