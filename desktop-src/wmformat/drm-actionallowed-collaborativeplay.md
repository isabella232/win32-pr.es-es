---
title: DRM_ActionAllowed_CollaborativePlay
description: El \_ atributo CollaborativePlay de DRM ActionAllowed \_ indica si la licencia permite reproducir el contenido en colaboración.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420307"
---
# <a name="drm_actionallowed_collaborativeplay"></a>\_CollaborativePlay ACTIONALLOWED \_ DRM

El **atributo \_ \_ CollaborativePlay de DRM ActionAllowed** indica si la licencia permite reproducir el contenido en colaboración.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

El derecho de reproducción colaborativa se aplica a la reproducción de contenido protegido como parte de una sesión de colaboración mediante servicios punto a punto. Por ejemplo, los usuarios de MSN Messenger 2004 pueden reproducir contenido protegido en una sesión de MusicMix. Este derecho solo se puede usar para contribuir a un archivo protegido en una sola sesión al mismo tiempo, y todos los usuarios que participan en la sesión deben estar en línea para representar el contenido.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




