---
title: DRM_HeaderSignPrivKey
description: La propiedad \_ HeaderSignPrivKey de DRM contiene la clave privada que se usa para firmar el encabezado asf.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey windows Media Format
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7f8cc90e509294d9de9d3577ad5a2d56b61eb3a471f9b493e555c0f1ecf824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547615"
---
# <a name="drm_headersignprivkey"></a>Encabezado \_ DRMSignPrivKey

La **propiedad \_ HeaderSignPrivKey de DRM** contiene la clave privada que se usa para firmar el encabezado asf.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Esta propiedad se genera mediante [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Mantenga este secreto de clave y comparta la clave pública solo con el servicio de licencia. Después de establecer esta clave, el componente DRM la usará para firmar el encabezado de archivo ASF (no el encabezado DRM que está firmado con los valores del objeto de firma digital, como DRM \_ LASignaturePrivKey). Obviamente, **el \_ encabezado DRMSignPrivKey** no se incluye en el encabezado de archivo.

Esta propiedad no es accesible desde el objeto de lector. Se puede establecer desde el objeto de escritor mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




