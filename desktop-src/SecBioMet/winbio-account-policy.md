---
title: Estructura de WINBIO_ACCOUNT_POLICY (Winbio \_ Adapter. h)
description: Contiene una directiva de suplantación predeterminada o específica de la cuenta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- Plataforma de biometría de Windows API de WINBIO_ACCOUNT_POLICY Structure
- PWINBIO_ACCOUNT_POLICY de puntero de estructura Plataforma de biometría de Windows API
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996387"
---
# <a name="winbio_account_policy-structure"></a>WINBIO \_ estructura de directiva de cuenta \_

La estructura de **\_ \_ Directiva de cuenta WINBIO** contiene una directiva de suplantación predeterminada o específica de la cuenta.

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

Estructura [**de \_ identidad de WINBIO**](winbio-identity.md) que especifica la información de la cuenta.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Uno de los valores de enumeración de [**acciones de directiva de WINBIO \_ anti \_ \_ \_ Spoofing**](winbio-anti-spoof-policy-action.md) que especifica qué acción de directiva de suplantación debe usar para la cuenta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Vea la explicación del método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obtener una descripción de cómo se usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Adapter. h (incluir Winbio \_ Adapter. h)</dt> </dl> |



 

 





