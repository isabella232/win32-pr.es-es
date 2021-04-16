---
title: DRM_IsDRMCached
description: La \_ propiedad IsDRMCached de DRM indica si la información de licencia de DRM versión 1 se ha almacenado en el equipo local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676347"
---
# <a name="drm_isdrmcached"></a>\_ISDRMCACHED DRM

La **propiedad \_ IsDRMCached de DRM** indica si la información de licencia de DRM versión 1 se ha almacenado en el equipo local.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Es **cierto** cuando la dirección URL de adquisición de licencias coincide con una de las dos direcciones URL conocidas que se usan para la adquisición de licencias local en DRM versión 1.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




