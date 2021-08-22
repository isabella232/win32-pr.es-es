---
title: DRM_DRMHeader_ContentDistributor
description: El atributo \_ DRMHeader ContentDistributor de DRM contiene una \_ cadena que identifica el distribuidor de contenido.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586465"
---
# <a name="drm_drmheader_contentdistributor"></a>DRM \_ DRMHeader \_ ContentDistributor

El **atributo \_ DRMHeader \_ ContentDistributor** de DRM contiene una cadena que identifica el distribuidor de contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El identificador de contenido es opcional y lo determina únicamente el creador del contenido. El objeto de escritor no hace nada con este atributo. Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




