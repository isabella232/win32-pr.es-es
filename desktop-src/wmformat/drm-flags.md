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
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360970"
---
# <a name="drm_flags"></a>Marcas \_ DRM

La **propiedad \_ Marcas DRM** se usa con contenido de la versión 1 de DRM solo para especificar los derechos que se incluirán en la licencia local. Los derechos se especifican con valores definidos por el tipo **de enumeración WMT \_ RIGHTS.** Se puede seleccionar más de un valor combinándolos con el operador **OR bit** a bit.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ Flags

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Al acceder a **la interfaz IWMHeaderInfo3** del objeto de escritor, puede agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura. Use [**IWMHeaderInfo::SetAttribute para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) establecer esta propiedad al crear contenido de la versión 1 de DRM.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




