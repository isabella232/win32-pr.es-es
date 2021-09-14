---
description: Permite que el Lector de origen use Media Foundation transformaciones (MFT) optimizadas para la transcodificación.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363918"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>ATRIBUTO \_ ENABLE \_ \_ \_ TRANSCODE ONLY \_ \_ TRANSFORMS de MF SOURCE READER ENABLE TRANSCODE ONLY

Permite que [el Lector de](source-reader.md) origen use Media Foundation transformaciones (MTA) optimizadas para la transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como booleano.

## <a name="remarks"></a>Observaciones

Algunas MTA, especialmente los descodificadores, están optimizadas para la transcodificación en lugar de para la reproducción. De forma predeterminada, el Lector de origen no cargará dichas transformaciones. Establezca este atributo en **TRUE** si desea usar MTA de transcodificación con el lector de origen.

Una aplicación podría establecer este atributo si no procesa los datos en tiempo real (para transcodificación o escenarios similares). De lo contrario, para la reproducción en tiempo real, use el comportamiento predeterminado.

Internamente, este atributo hace que el lector de origen incluya la marca **\_ MFT ENUM \_ FLAG \_ TRANSCODE \_ ONLY** cuando llama a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




