---
title: WMDRMNET_POLICY estructura (wmdrmsdk. h)
description: La \_ estructura de directiva WMDRMNET contiene la Directiva que se va a usar para DRM de Windows Media para las operaciones de dispositivos de red.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649525"
---
# <a name="wmdrmnet_policy-structure"></a>Estructura de directiva de WMDRMNET \_

La estructura de **\_ Directiva WMDRMNET** contiene la Directiva que se va a usar para DRM de Windows Media para las operaciones de dispositivos de red.

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

Miembro de la enumeración de [**\_ \_ tipo de directiva WMDRMNET**](wmdrmnet-policy-type.md) que especifica el tipo de directiva.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Búfer que contiene la Directiva. El único tipo de directiva que se admite actualmente es el **\_ tipo de directiva WMDRMNET \_ \_ TRANSCRYPTPLAY**. Este miembro es un puntero a una estructura de **\_ \_ TRANSCRYPTPLAY de directiva de WMDRMNET** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa como parámetro para el método [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> <dt>

[**\_ \_ requisitos globales de la Directiva WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**\_ \_ entorno mínimo de directiva de WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**\_TRANSCRYPTPLAY de directiva de WMDRMNET \_**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**\_tipo de directiva WMDRMNET \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





