---
title: DRM_ActionAllowed_CollaborativePlay
description: El atributo ActionAllowed CollaborativePlay de DRM indica si la licencia permite reproducir el \_ \_ contenido de forma colaborativa.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467097"
---
# <a name="drm_actionallowed_collaborativeplay"></a>Acción \_ drmAllowed \_ CollaborativePlay

El **atributo \_ ActionAllowed \_ CollaborativePlay de DRM** indica si la licencia permite reproducir el contenido de forma colaborativa.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Observaciones

El derecho de juego colaborativo se aplica a la reproducción de contenido protegido como parte de una sesión de colaboración mediante servicios punto a punto. Por ejemplo, los usuarios de MSN Messenger 2004 pueden reproducir contenido protegido en una sesión de MusicMix. Este derecho solo se puede usar para contribuir con un archivo protegido a una sola sesión a la vez, y todos los usuarios que participan en la sesión deben estar en línea para representar el contenido.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




