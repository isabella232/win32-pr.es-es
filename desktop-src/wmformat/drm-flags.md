---
title: DRM_Flags
description: La propiedad Marcas DRM se usa con contenido de la versión 1 de DRM solo para especificar los derechos que se \_ incluirán en la licencia local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags windows Media Format
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf4f1b2065eb1b251f0c555f8c33e424e43aefd04377ed894edb90c121aacb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086016"
---
# <a name="drm_flags"></a>Marcas \_ DRM

La **propiedad Marcas DRM \_ se** usa con contenido de la versión 1 de DRM solo para especificar los derechos que se incluirán en la licencia local. Los derechos se especifican con valores definidos por el tipo **de enumeración WMT \_ RIGHTS.** Se puede seleccionar más de un valor combinándolos con el operador **OR bit** a bit.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ Flags

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Al acceder a **la interfaz IWMHeaderInfo3** del objeto de escritor, puede agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura. Use [**IWMHeaderInfo::SetAttribute para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) establecer esta propiedad al crear contenido de la versión 1 de DRM.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




