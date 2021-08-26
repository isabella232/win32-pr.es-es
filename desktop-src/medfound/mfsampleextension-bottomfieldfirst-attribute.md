---
description: Especifica la dominación de campo para un fotograma de vídeo entrelazado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113075"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>Atributo MFSampleExtension \_ BottomFieldFirst

Especifica la dominación de campo para un fotograma de vídeo entrelazado. Este atributo se aplica a los ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

Si el fotograma de vídeo está entrelazado y el ejemplo contiene dos campos intercalados, este atributo indica qué campo se muestra primero. Si **es TRUE,** el campo inferior es el primero en el tiempo. Si **es FALSE,** el campo superior es el primero.

Si el marco está entrelazado y el ejemplo contiene un solo campo, este atributo indica qué campo contiene la muestra. Si **es TRUE,** el ejemplo contiene el campo inferior. Si **es FALSE,** el ejemplo contiene el campo superior.

Si el marco es progresiva, este atributo describe cómo se deben ordenar los campos cuando la salida está entrelazada. Si **es TRUE,** el campo inferior debe generarse primero. Si **es FALSE,** primero se debe generar el campo superior.

Si no se establece este atributo, el tipo de medio describe la dominación del campo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




