---
description: Establece el valor máximo &\# 0034;leaky bucket&\# 0034; parámetros (consulte Comentarios) para codificar un archivo Windows Media. Estos parámetros se usan para la velocidad de bits máxima. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2 atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060845"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>Atributo MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2

Establece los parámetros máximos del "cubo de fugas" (consulte Comentarios) para codificar un Windows multimedia. Estos parámetros se usan para la velocidad de bits máxima. Establezca este atributo mediante la interfaz [**IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El valor de este atributo es una matriz de tres **DWORD,** en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Ventana búfer, en milisegundos.
-   Integridad inicial del búfer, en bytes.

Para obtener más información sobre el concepto de cubo de pérdida, vea el tema [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) en la documentación del SDK Windows Media Format.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ASF](asf-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




