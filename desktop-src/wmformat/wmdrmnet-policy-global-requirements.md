---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS estructura (Wmdrmsdk.h)
description: La estructura DE REQUISITOS GLOBALES DE WMDRMNET POLICY contiene los requisitos globales \_ para Windows DRM multimedia para \_ \_ dispositivos de red.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS estructura windows Formato multimedia
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843976"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>ESTRUCTURA DE REQUISITOS GLOBALES DE WMDRMNET \_ POLICY \_ \_

La **estructura GLOBAL \_ \_ \_ REQUIREMENTS de WMDRMNET POLICY** contiene los requisitos globales para Windows DRM multimedia para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_ ESTRUCTURA \_ DE ENTORNO MÍNIMO \_ DE**](wmdrmnet-policy-minimum-environment.md) DIRECTIVA que contiene los requisitos mínimos de seguridad Windows DRM multimedia para dispositivos de red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**DIRECTIVA \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





