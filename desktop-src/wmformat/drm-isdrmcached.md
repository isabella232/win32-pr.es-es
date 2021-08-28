---
title: DRM_IsDRMCached
description: La propiedad ISDRMCached de DRM indica si la información de licencia de DRM versión 1 se ha almacenado \_ en el equipo local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached windows Media Format
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9b5bbcf7e4e1c11c8ae992156b7541ac66c7a9d43f2cb1d52878d1ee6762d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709045"
---
# <a name="drm_isdrmcached"></a>DRM \_ IsDRMCached

La **propiedad \_ ISDRMCached de DRM** indica si la información de licencia de DRM versión 1 se ha almacenado en el equipo local.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Es TRUE **cuando la dirección** URL de adquisición de licencias coincide con una de las dos direcciones URL de conocimiento que se usan para la adquisición de licencias locales en la versión 1 de DRM.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




