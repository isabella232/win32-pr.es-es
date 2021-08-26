---
description: Contiene datos de formato adicionales para un tipo de medio.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0196e8fea06bb84fe5a78a8b486f95864e0c6d889692dfa6f3ee9b1103da518a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012794"
---
# <a name="mf_mt_user_data-attribute"></a>Atributo MF \_ MT \_ USER \_ DATA

Contiene datos de formato adicionales para un tipo de medio.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El significado de los datos de este atributo depende del formato descrito por el tipo de medio.



| Tipo de formato                                                                                                           | Datos de formato adicionales                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Códec multimedia.                                                                                                  | Códec de datos privados.                                                                                                                       |
| Estructura [**VIDEOINFOHEADER o**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) convertida.   | Datos adicionales que aparecen después de la [**estructura BITMAPINFOHEADER,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sin incluir la tabla de colores ni las máscaras de color. |
| Estructura [**CONversa DESATEX**](/previous-versions/dd757713(v=vs.85)) [**o DESATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) convertida. | Datos adicionales que aparecen después de la estructura de formato de audio.                                                                                 |



 

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

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
