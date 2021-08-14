---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT estructura (Wmdrmsdk.h)
description: La estructura DE ENTORNO MÍNIMO DE DIRECTIVA DE WMDRMNET contiene los requisitos mínimos de seguridad Windows DRM de multimedia \_ \_ para \_ dispositivos de red.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027466"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>ESTRUCTURA DE ENTORNO MÍNIMO DE DIRECTIVA DE WMDRMNET \_ \_ \_

La estructura DE ENTORNO MÍNIMO DE **\_ DIRECTIVA \_ DE \_ WMDRMNET** contiene los requisitos mínimos de seguridad Windows DRM de multimedia para dispositivos de red.

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

Nivel mínimo de seguridad de la aplicación requerido.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

Versión mínima de la lista de revocación de certificados de aplicación requerida.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

Lista mínima de revocación de certificados de dispositivo requerida.

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

[**DIRECTIVA DE \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





