---
title: DRM_IndividualizedVersion
description: El atributo DRM IndividualizedVersion se almacena en el encabezado DRM y contiene la versión individualizada mínima \_ necesaria para acceder al contenido.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion windows Media Format
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704687"
---
# <a name="drm_individualizedversion"></a>DRM \_ IndividualizedVersion

El **atributo DRM \_ IndividualizedVersion** se almacena en el encabezado DRM y contiene la versión individualizada mínima necesaria para acceder al contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente con contenido drm versión 7. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). El mismo atributo de archivo se puede recuperar mediante [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




