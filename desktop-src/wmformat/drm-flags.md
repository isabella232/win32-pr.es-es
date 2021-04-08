---
title: DRM_Flags
description: La \_ propiedad marcas DRM se usa solo con contenido de la versión 1 de DRM para especificar los derechos que se incluirán en la licencia local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994943"
---
# <a name="drm_flags"></a>\_Marcas DRM

La **propiedad \_ marcas DRM** se usa solo con contenido de la versión 1 de DRM para especificar los derechos que se incluirán en la licencia local. Los derechos se especifican con valores definidos por el tipo de enumeración de **\_ derechos WMT** . Se puede seleccionar más de un valor combinándolos con el operador bit a bit **or** .

## <a name="global-constant"></a>Constante global

g \_ marcas de wszWMDRM \_

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor. En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura. Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad al crear el contenido de la versión 1 de DRM.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




