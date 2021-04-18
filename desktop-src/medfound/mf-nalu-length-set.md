---
description: Indica que la información de longitud de NALU se enviará como un BLOB con cada ejemplo H. 264 comprimido.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697760"
---
# <a name="mf_nalu_length_set-attribute"></a>\_Atributo de \_ conjunto de longitud MF Nalu \_

Indica que la información de longitud de NALU se enviará como un **BLOB** con cada ejemplo H. 264 comprimido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Establezca este atributo en el tipo de medio de entrada de MEDIASUBTYPE \_ H264.

Establezca MF \_ Nalu \_ longitud \_ establecida en el tipo de medio de entrada del descodificador H. 264, que indica que cada ejemplo de entrada tendrá una longitud Nalu disponible y que cada ejemplo de entrada contenga una imagen principal completa.

El **BLOB** que contiene la información de longitud de Nalu se puede recuperar del atributo de [ \_ información de \_ longitud \_ MF Nalu](mf-nalu-length-information.md) en el ejemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




