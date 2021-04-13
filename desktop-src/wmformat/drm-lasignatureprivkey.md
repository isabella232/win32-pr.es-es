---
title: DRM_LASignaturePrivKey
description: La \_ propiedad LASignaturePrivKey de DRM contiene la clave privada que se usa para cifrar el encabezado DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420309"
---
# <a name="drm_lasignatureprivkey"></a>\_LASIGNATUREPRIVKEY DRM

La **propiedad \_ LASignaturePrivKey de DRM** contiene la clave privada que se usa para cifrar el encabezado DRM.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Esta propiedad se puede generar mediante el método [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) . Esta propiedad debe ser un secreto conocido solo por el creador del contenido. Esta propiedad se puede establecer con el método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) . No es accesible para el objeto lector.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




