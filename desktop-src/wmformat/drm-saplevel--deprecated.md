---
title: DRM_SAPLEVEL (desusado)
description: Especifica el nivel de la ruta de acceso de audio seguro (SAP) admitido por la aplicación.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (en desuso) formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649467"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (desusado)

\[**DRM \_ SAPLEVEL** ya no está disponible para su uso a partir de Windows Vista. En su lugar, use el audio de modo de usuario protegido (PUMA) en la biblioteca de Media Foundation. \]

La **propiedad \_ SAPLEVEL de DRM** especifica el nivel de la ruta de acceso de audio seguro (SAP) admitido por la aplicación.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de solo escritura que se establece mediante una llamada a [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). El valor es una representación de cadena de caracteres anchos del nivel de SAP, como L "200". Los valores admitidos actualmente son 200 y 300.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|--------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows XP<br/>          |
| Fin de compatibilidad de servidor<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





