---
description: Indica que la información de longitud de NALU se enviará como un BLOB con cada ejemplo de H.264 comprimido.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360698"
---
# <a name="mf_nalu_length_set-attribute"></a>Atributo MF \_ NALU \_ LENGTH \_ SET

Indica que la información de longitud de NALU se enviará como **un BLOB** con cada ejemplo de H.264 comprimido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Establezca este atributo en el tipo de medio de entrada MEDIASUBTYPE \_ H264.

Establezca MF NALU LENGTH SET en el tipo de medio de entrada del descodificador \_ \_ H.264, lo que indica que cada muestra de entrada tendrá una longitud naLU disponible y cada muestra de entrada contiene una imagen principal \_ completa.

El **BLOB** que contiene la información de longitud de NALU se puede recuperar del atributo [MF \_ NALU LENGTH \_ \_ INFORMATION](mf-nalu-length-information.md) en el ejemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




