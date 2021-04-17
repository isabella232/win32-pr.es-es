---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT estructura (wmdrmsdk. h)
description: La \_ estructura de entorno mínima de la Directiva WMDRMNET \_ \_ contiene los requisitos de seguridad mínimos para DRM de Windows Media para dispositivos de red.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699978"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_Estructura de \_ entorno mínima de directiva de WMDRMNET \_

La estructura de **\_ \_ \_ entorno mínima de la Directiva WMDRMNET** contiene los requisitos de seguridad mínimos para DRM de Windows Media para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

Nivel de seguridad de la aplicación mínimo requerido.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

Versión de lista de revocación de certificados de aplicación mínima requerida.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

Se requiere una lista de revocación de certificados de dispositivo mínima.

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

 

 





