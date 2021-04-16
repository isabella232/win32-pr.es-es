---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS estructura (wmdrmsdk. h)
description: La \_ estructura de \_ requisitos globales de la Directiva WMDRMNET \_ contiene los requisitos globales de DRM de Windows Media para dispositivos de red.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699336"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_Estructura de \_ \_ los requisitos globales de la Directiva WMDRMNET

La estructura de **\_ \_ \_ requisitos globales de la Directiva WMDRMNET** contiene los requisitos globales de DRM de Windows Media para dispositivos de red.

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

[**WMDRMNET \_ Directiva estructura \_ mínima de \_ entorno**](wmdrmnet-policy-minimum-environment.md) que contiene los requisitos de seguridad mínimos para Windows Media DRM para dispositivos de red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**\_Directiva WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





