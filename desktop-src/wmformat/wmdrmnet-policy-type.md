---
title: WMDRMNET_POLICY_TYPE enumeración (Wmdrmsdk.h)
description: El tipo de enumeración WMDRMNET POLICY TYPE enumera los tipos de directivas que están disponibles para Windows DRM multimedia \_ \_ para operaciones de dispositivos de red.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE enumeración windows Media Format
- enumeración windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aec574717abb51117b142b8450ad7548d84766b4138f76a4296982422462fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697817"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>Enumeración WMDRMNET \_ POLICY \_ TYPE

El **tipo de enumeración WMDRMNET \_ POLICY \_ TYPE** enumera los tipos de directivas que están disponibles para Windows DRM multimedia para operaciones de dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**TIPO DE DIRECTIVA WMDRMNET \_ \_ SIN \_ DEFINIR**
</dt> <dd>

No se admiten tipos de directiva no definidos.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**TRANSCRYPTPLAY \_ DEL TIPO \_ DE DIRECTIVA \_ WMDRMNET**
</dt> <dd>

La directiva rige la capacidad de convertir contenido protegido por drm multimedia de Windows en DRM multimedia de Windows protegido para los datos de dispositivos de red y reproducirlo en un dispositivo en red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> <dt>

[**DIRECTIVA DE \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





