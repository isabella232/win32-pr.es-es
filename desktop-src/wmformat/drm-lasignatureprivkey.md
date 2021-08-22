---
title: DRM_LASignaturePrivKey
description: La propiedad \_ DRM LASignaturePrivKey contiene la clave privada que se usa para cifrar el encabezado DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey windows Media Format
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704329"
---
# <a name="drm_lasignatureprivkey"></a>DRM \_ LASignaturePrivKey

La **propiedad \_ DRM LASignaturePrivKey** contiene la clave privada que se usa para cifrar el encabezado DRM.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Esta propiedad se puede generar mediante el [**método IWMDRMWriter::GenerateSigningKeyPair.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) Esta propiedad debe seguir siendo un secreto conocido solo por el creador del contenido. Esta propiedad se puede establecer con el [**método IWMDRMWriter::SetDRMAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) No es accesible para el objeto de lector.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




