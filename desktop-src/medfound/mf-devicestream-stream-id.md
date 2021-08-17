---
description: Especifica el identificador de streaming de kernel (KS) para una secuencia en un dispositivo de captura de vídeo.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: MF_DEVICESTREAM_STREAM_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb5b4004ae2e280806411e51f7adfe83f9a4f28d71103a3d3c6e9a247f2011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973854"
---
# <a name="mf_devicestream_stream_id-attribute"></a>Atributo \_ MF DEVICESTREAM \_ STREAM \_ ID

Especifica el identificador de streaming de kernel (KS) para una secuencia en un dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Para obtener este atributo, haga lo siguiente:

1.  Consulte el origen de medios para la [**interfaz IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
2.  Llame [**a IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.
3.  Llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




