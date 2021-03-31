---
title: Estructura de WINBIO_ANTI_SPOOF_POLICY (Winbio \_ Types. h)
description: Representa la Directiva de antifalsificación para un usuario.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- Plataforma de biometría de Windows API de WINBIO_ANTI_SPOOF_POLICY Structure
- PWINBIO_ANTI_SPOOF_POLICY de puntero de estructura Plataforma de biometría de Windows API
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
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491392"
---
# <a name="winbio_anti_spoof_policy-structure"></a>Estructura de directiva de WINBIO \_ anti \_ Spoofing \_

Representa la Directiva de antifalsificación para un usuario.

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

El tipo de acción que se debe realizar para la Directiva de antifalsificación.

</dd> <dt>

**Origen**
</dt> <dd>

Origen de la Directiva de antifalsificación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_origen de directiva de WINBIO \_**](winbio-policy-source.md)
</dt> <dt>

[**\_resultado asincrónico de WINBIO \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





