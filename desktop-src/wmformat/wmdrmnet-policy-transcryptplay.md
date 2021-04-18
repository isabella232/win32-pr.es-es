---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY estructura (wmdrmsdk. h)
description: La estructura WMDRMNET de la \_ directiva \_ de TRANSCRYPTPLAY contiene la información de la Directiva para reproducir contenido con DRM de Windows Media para dispositivos de red.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649528"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_ \_ Estructura TRANSCRYPTPLAY de la Directiva WMDRMNET

La estructura WMDRMNET de la **\_ Directiva de \_ TRANSCRYPTPLAY** contiene la información de la Directiva para reproducir contenido con DRM de Windows Media para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**GLOBALS**
</dt> <dd>

Estructura global de directivas.

</dd> <dt>

**playOPLs**
</dt> <dd>

Niveles de protección de salida para la reproducción. **WMDRMNET \_ La Directiva de \_ \_ OPL de Play** es un tipo definido como el [**OPL de reproducción de DRM \_ \_ \_**](drm-play-opl-ex.md).

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

 

 





