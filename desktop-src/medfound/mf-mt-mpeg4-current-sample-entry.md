---
description: Especifica la entrada actual en el cuadro Descripción del ejemplo para un tipo de medio MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648517"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>\_Atributo de \_ entrada de ejemplo de MPEG4 \_ actual \_ \_ de MF MT

Especifica la entrada actual en el cuadro Descripción del ejemplo para un tipo de medio MPEG-4.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

En un archivo MP4 o 3GP, el cuadro Descripción del ejemplo describe la codificación utilizada para una secuencia en el archivo. El cuadro Descripción del ejemplo puede contener varias entradas. Este atributo especifica la entrada que se va a usar. El valor es un índice basado en cero en la lista.

Actualmente, el único valor admitido es 0. El atributo se ha definido para la extensibilidad futura.

El origen de archivo MPEG-4 siempre establece el valor en 0. Los receptores de archivos MP4 y 3GP omiten el valor de este atributo si está presente.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[\_Descripción del \_ ejemplo de MPEG4 MT \_ de MF \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




