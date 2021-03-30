---
description: Especifica el ámbito del campo de un fotograma de vídeo entrelazado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360572"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>\_Atributo BottomFieldFirst de MFSampleExtension

Especifica el ámbito del campo de un fotograma de vídeo entrelazado. Este atributo se aplica a los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Si el fotograma de vídeo está entrelazado y el ejemplo contiene dos campos intercalados, este atributo indica el campo que se muestra en primer lugar. Si es **true**, el campo inferior es el primero en el tiempo. Si es **false**, el campo superior es primero.

Si el marco está entrelazado y el ejemplo contiene un campo único, este atributo indica el campo que contiene el ejemplo. Si **es true**, el ejemplo contiene el campo inferior. Si **es false**, el ejemplo contiene el campo superior.

Si el marco es progresivo, este atributo describe cómo se deben ordenar los campos cuando la salida está entrelazada. Si **es true**, el campo inferior debe generarse primero. Si **es false**, el campo superior se debe mostrar primero.

Si no se establece este atributo, el tipo de medio describe el ámbito de los campos.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




