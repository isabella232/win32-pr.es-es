---
title: DRM_IndividualizedVersion
description: El atributo IndividualizedVersion de DRM se almacena en el encabezado DRM y contiene la versión individualizada mínima \_ necesaria para acceder al contenido.
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
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247376"
---
# <a name="drm_individualizedversion"></a>DRM \_ IndividualizedVersion

El **atributo \_ IndividualizedVersion** de DRM se almacena en el encabezado DRM y contiene la versión individualizada mínima necesaria para acceder al contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). El mismo atributo de archivo se puede recuperar mediante [**\_ DRMHeader \_ IndividualizedVersion de DRM.**](drm-drmheader-individualizedversion.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




