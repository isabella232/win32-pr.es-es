---
title: DRM_SAPLEVEL (en desuso)
description: Especifica el nivel de ruta de acceso de audio segura (SAP) compatible con la aplicación.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (en desuso) Windows Media Format
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930895"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (en desuso)

\[**DRM \_ SAPLEVEL** ya no está disponible para su uso a Windows Vista. En su lugar, use audio en modo de usuario protegido (VMM) en la biblioteca Media Foundation usuario. \]

La **propiedad \_ SAPLEVEL de DRM** especifica el nivel de ruta de acceso de audio seguro (SAP) compatible con la aplicación.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Se trata de una propiedad de solo escritura que se establece mediante una llamada a [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). El valor es una representación de cadena de caracteres anchos del nivel de SAP, como L"200". Los valores admitidos actuales son 200 y 300.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|--------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows XP<br/>          |
| Fin de compatibilidad de servidor<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





