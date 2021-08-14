---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY estructura (Wmdrmsdk.h)
description: La estructura TRANSCRYPTPLAY de WMDRMNET POLICY contiene la información de directiva para reproducir contenido mediante Windows DRM multimedia \_ \_ para dispositivos de red.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY windows Media Format de estructura
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195510"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>Estructura TRANSCRYPTPLAY de LA \_ DIRECTIVA \_ WMDRMNET

La **estructura \_ \_ TRANSCRYPTPLAY de WMDRMNET POLICY** contiene la información de directiva para reproducir contenido mediante Windows DRM multimedia para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Globals**
</dt> <dd>

Estructura de directiva global.

</dd> <dt>

**playOPLs**
</dt> <dd>

Niveles de protección de salida para la reproducción. **WMDRMNET \_ POLICY \_ PLAY \_ OPL** es un tipo definido como [**DRM PLAY \_ \_ OPL \_ EX**](drm-play-opl-ex.md).

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

 

 





