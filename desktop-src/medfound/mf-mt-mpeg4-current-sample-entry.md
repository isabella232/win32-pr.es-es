---
description: Especifica la entrada actual en el cuadro de descripción de ejemplo para un tipo de medio MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269140"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>Atributo MF \_ MT \_ MPEG4 \_ CURRENT SAMPLE \_ \_ ENTRY

Especifica la entrada actual en el cuadro de descripción de ejemplo para un tipo de medio MPEG-4.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

En un archivo MP4 o 3GP, el cuadro de descripción de ejemplo describe la codificación usada para una secuencia en el archivo. El cuadro de descripción de ejemplo puede contener varias entradas. Este atributo especifica qué entrada se va a usar. El valor es un índice de base cero en la lista.

Actualmente, el único valor admitido es 0. El atributo se ha definido para la extensibilidad futura.

El origen de archivo MPEG-4 siempre establece el valor en 0. Los receptores de archivos MP4 y 3GP omiten el valor de este atributo si está presente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows aplicaciones de escritorio 7 \[ \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[DESCRIPCIÓN \_ DEL \_ EJEMPLO MPEG4 \_ DE \_ MF MT](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




