---
title: WINBIO_ACCOUNT_POLICY estructura (Winbio \_ adapter.h)
description: Contiene una directiva de antispoofing predeterminada o específica de la cuenta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY estructura Windows API de marco biométrico
- PWINBIO_ACCOUNT_POLICY puntero de estructura Windows API de marco biométrico
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
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035255"
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



## <a name="members"></a>Miembros

<dl> <dt>

**Identidad**
</dt> <dd>

Estructura [**DE WINBIO \_ IDENTITY**](winbio-identity.md) que especifica la información de la cuenta.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Uno de los valores de enumeración DE ACCIÓN DE DIRECTIVA [**\_ DE \_ SPOOF \_ \_**](winbio-anti-spoof-policy-action.md) ANTI DE WINBIO que especifica qué acción de directiva de antispoofing se va a usar para la cuenta.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Consulte la explicación del método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obtener una descripción de cómo se usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ adapter.h (incluir Winbio \_ adapter.h)</dt> </dl> |



 

 





