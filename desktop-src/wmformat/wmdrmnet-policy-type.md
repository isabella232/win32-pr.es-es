---
title: Enumeración WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración de tipo de directiva WMDRMNET muestra los tipos de directivas que están disponibles para las operaciones de Windows Media DRM para dispositivos de red.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE enumeración formato de Windows Media
- enumeración Windows Media Format
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
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649988"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>\_Enumeración de tipo de directiva WMDRMNET \_

El tipo de enumeración de **\_ \_ tipo de directiva WMDRMNET** muestra los tipos de directivas que están disponibles para las operaciones de Windows Media DRM para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_tipo de directiva WMDRMNET \_ sin \_ definir**
</dt> <dd>

No se admiten tipos de directivas no definidos.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo de directiva WMDRMNET \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

La Directiva rige la capacidad de convertir contenido protegido por DRM de Windows Media en Windows Media DRM protegido para los datos de dispositivos de red y reproducirlo en un dispositivo en red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> <dt>

[**\_Directiva WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





