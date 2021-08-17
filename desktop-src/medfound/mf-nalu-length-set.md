---
description: Indica que la información de longitud de NALU se enviará como blob con cada ejemplo de H.264 comprimido.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104391"
---
# <a name="mf_nalu_length_set-attribute"></a>Atributo MF \_ NALU \_ LENGTH \_ SET

Indica que la información de longitud de NALU se enviará como **blob** con cada ejemplo de H.264 comprimido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Establezca este atributo en el tipo de medio de entrada MEDIASUBTYPE \_ H264.

Establezca MF NALU LENGTH SET en el tipo de medio de entrada del descodificador \_ \_ H.264, lo que indica que cada muestra de entrada tendrá una longitud NALU disponible y cada muestra de entrada contiene una imagen principal \_ completa.

El **BLOB** que contiene la información de longitud de NALU se puede recuperar del atributo [MF \_ NALU LENGTH \_ \_ INFORMATION](mf-nalu-length-information.md) en el ejemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




