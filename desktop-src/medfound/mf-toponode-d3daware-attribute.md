---
description: Especifica si la transformación asociada a un nodo de topología admite la aceleración de vídeo de DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498112"
---
# <a name="mf_toponode_d3daware-attribute"></a>\_ \_ Atributo D3DAWARE de MF TOPONODE

Especifica si la transformación asociada a un nodo de topología admite la aceleración de vídeo de DirectX (DXVA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).

Normalmente, las aplicaciones no usan este atributo directamente. La sesión de medios establece este atributo en un nodo de transformación si la transformación de Media Foundation subyacente tiene el atributo [**MF \_ \_ \_ compatible**](mf-sa-d3d-aware-attribute.md) con el D3D de la SA.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




