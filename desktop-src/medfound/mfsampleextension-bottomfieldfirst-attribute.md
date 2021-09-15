---
description: Especifica la dominación de campo para un fotograma de vídeo entrelazado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360685"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>Atributo MFSampleExtension \_ BottomFieldFirst

Especifica la dominación de campo para un fotograma de vídeo entrelazado. Este atributo se aplica a los ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Si el fotograma de vídeo está entrelazado y el ejemplo contiene dos campos intercalados, este atributo indica qué campo se muestra primero. Si **es TRUE,** el campo inferior es el primero en el tiempo. Si **es FALSE,** el campo superior es el primero.

Si el marco está entrelazado y el ejemplo contiene un solo campo, este atributo indica qué campo contiene la muestra. Si **es TRUE,** el ejemplo contiene el campo inferior. Si **es FALSE,** el ejemplo contiene el campo superior.

Si el marco es progresiva, este atributo describe cómo se deben ordenar los campos cuando se entrelaza la salida. Si **es TRUE,** primero se debe generar el campo inferior. Si **es FALSE,** primero se debe generar el campo superior.

Si no se establece este atributo, el tipo de medio describe la dominación de campo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




