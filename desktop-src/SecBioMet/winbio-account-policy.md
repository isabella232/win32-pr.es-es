---
title: WINBIO_ACCOUNT_POLICY estructura (Winbio \_ adapter.h)
description: Contiene una directiva de antispoofing predeterminada o específica de la cuenta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY de Windows API de Biometric Framework
- PWINBIO_ACCOUNT_POLICY puntero de estructura Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071180"
---
# <a name="winbio_account_policy-structure"></a>Estructura DE \_ DIRECTIVA DE \_ CUENTAS WINBIO

La **estructura DIRECTIVA DE CUENTA \_ \_ WINBIO** contiene una directiva de antispoofing predeterminada o específica de la cuenta.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Members

<dl> <dt>

**Identidad**
</dt> <dd>

Estructura [**WINBIO \_ IDENTITY que**](winbio-identity.md) especifica la información de la cuenta.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Uno de los valores de enumeración ACCIÓN DE DIRECTIVA ANTI [**\_ \_ SPOOF \_ \_**](winbio-anti-spoof-policy-action.md) DE WINBIO que especifica qué acción de directiva de antispoofing se va a usar para la cuenta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Consulte la explicación del método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obtener una descripción de cómo se usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ adapter.h (incluir Winbio \_ adapter.h)</dt> </dl> |



 

 





