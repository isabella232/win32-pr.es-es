---
description: Establece el promedio &\# 0034;leaky bucket&\# 0034; parámetros (consulte Comentarios) para codificar un archivo Windows Media. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET1 atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5343d7721d6fad4be4d8623ffdd8f1b3e63fccbe8d90cd4616e0115c35fc2100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826825"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>Atributo MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1

Establece el promedio de parámetros de "cubo de pérdida" (consulte Comentarios) para codificar un Windows multimedia. Establezca este atributo mediante la interfaz [**IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El valor de este atributo es una matriz de tres **DWORD,** en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Ventana búfer, en milisegundos.
-   Integridad inicial del búfer, en bytes.

Para obtener más información sobre el concepto de cubo con pérdidas, consulte el tema [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) en la documentación del SDK Windows Media Format.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




