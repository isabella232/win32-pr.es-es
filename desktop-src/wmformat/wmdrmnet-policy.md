---
title: WMDRMNET_POLICY estructura (Wmdrmsdk.h)
description: La estructura DE DIRECTIVA DE WMDRMNET contiene la directiva que se usará para Windows DRM multimedia para las operaciones \_ de dispositivos de red.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY estructura windows Media Format
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf648ef5e300fa9fef1cf12fd4698f4ec196f62130bf75a02f263cd96931f0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653428"
---
# <a name="wmdrmnet_policy-structure"></a>Estructura DE DIRECTIVA \_ DE WMDRMNET

La **estructura DE DIRECTIVA \_ DE WMDRMNET** contiene la directiva que se usará para Windows DRM multimedia para las operaciones de dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ePolicyType**
</dt> <dd>

Miembro de la [**enumeración WMDRMNET \_ POLICY \_ TYPE**](wmdrmnet-policy-type.md) que especifica el tipo de directiva.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Búfer que contiene la directiva. El único tipo de directiva admitido actualmente **es WMDRMNET \_ POLICY TYPE \_ \_ TRANSCRYPTPLAY**. Este miembro es un puntero a una **estructura \_ \_ TRANSCRYPTPLAY de WMDRMNET POLICY.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa como parámetro para el [**método IWMDRMNetTransmitter::GetLeafLicenseResponse.**](iwmdrmnettransmitter-getleaflicenseresponse.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**REQUISITOS GLOBALES DE LA \_ DIRECTIVA WMDRMNET \_ \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**ENTORNO MÍNIMO DE DIRECTIVA \_ DE WMDRMNET \_ \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**TRANSCRYPTPLAY DE \_ DIRECTIVA \_ WMDRMNET**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**TIPO DE DIRECTIVA \_ \_ WMDRMNET**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





