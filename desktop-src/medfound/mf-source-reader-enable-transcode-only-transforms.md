---
description: Permite al lector de código fuente usar transformaciones de Media Foundation (MFTs) que están optimizadas para la transcodificación.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541347"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>\_Lector de código fuente MF \_ \_ Habilitar solo el \_ \_ \_ atributo transformaciones

Permite al [lector de código fuente](source-reader.md) usar transformaciones de Media Foundation (MFTs) que están optimizadas para la transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como booleanos.

## <a name="remarks"></a>Observaciones

Algunos MFTs, especialmente los descodificadores, están optimizados para la transcodificación en lugar de la reproducción. De forma predeterminada, el lector de origen no cargará dichas transformaciones. Establezca este atributo en **true** si desea usar la transcodificación de MFTs con el lector de origen.

Una aplicación podría establecer este atributo si no procesa los datos en tiempo real (para la transcodificación o escenarios similares). De lo contrario, para la reproducción en tiempo real, utilice el comportamiento predeterminado.

Internamente, este atributo hace que el lector de origen incluya la marca de **\_ enumeración de MFT \_ \_ \_ solo Transcode** Flag cuando llama a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




