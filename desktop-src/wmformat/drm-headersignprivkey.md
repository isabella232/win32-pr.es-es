---
title: DRM_HeaderSignPrivKey
description: La \_ propiedad HeaderSignPrivKey de DRM contiene la clave privada utilizada para firmar el encabezado ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788757"
---
# <a name="drm_headersignprivkey"></a>\_HEADERSIGNPRIVKEY DRM

La **propiedad \_ HeaderSignPrivKey de DRM** contiene la clave privada utilizada para firmar el encabezado ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Esta propiedad se genera mediante [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Mantenga esta clave secreta y comparta la clave pública solo con el servicio de licencias. Después de establecer esta clave, el componente DRM la usará para firmar el encabezado del archivo ASF (no el encabezado DRM que está firmado con los valores del objeto de firma digital como \_ LASIGNATUREPRIVKEY DRM). Obviamente, **DRM \_ HeaderSignPrivKey** no se incluye en el encabezado del archivo.

No se puede obtener acceso a esta propiedad desde el objeto de lector. Se puede establecer desde el objeto escritor mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




