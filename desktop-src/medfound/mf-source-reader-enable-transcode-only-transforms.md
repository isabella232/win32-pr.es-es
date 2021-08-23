---
description: Permite que el Lector de origen use Media Foundation transformaciones (MTA) optimizadas para la transcodificación.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc5362c93138ef301ac65ace799ad64d59ac9110af349822e0efa98d410686e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605022"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>Atributo ENABLE \_ \_ \_ \_ TRANSCODE \_ ONLY \_ TRANSFORMS del LECTOR DE ORIGEN DE MF

Permite que [el Lector de](source-reader.md) origen use Media Foundation transformaciones (MTA) optimizadas para la transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como booleano.

## <a name="remarks"></a>Comentarios

Algunas MTA, especialmente los descodificadores, están optimizadas para la transcodificación en lugar de la reproducción. De forma predeterminada, el Lector de origen no cargará dichas transformaciones. Establezca este atributo en **TRUE** si desea usar MTA de transcodificación con el Lector de origen.

Una aplicación podría establecer este atributo si no procesa los datos en tiempo real (para la transcodificación o escenarios similares). De lo contrario, para la reproducción en tiempo real, use el comportamiento predeterminado.

Internamente, este atributo hace que el Lector de origen incluya la marca **\_ \_ \_ TRANSCODE \_ ONLY de MFT ENUM FLAG** cuando llama a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




