---
description: Especifica la duración de una secuencia de bytes, en unidades de 100 nanosegundos.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION atributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ba32b394fa776b5b70a5a649292ffa205132645b15c24a57591483c734b238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826735"
---
# <a name="mf_bytestream_duration-attribute"></a>Atributo \_ MF BYTESTREAM \_ DURATION

Especifica la duración de una secuencia de bytes, en unidades de 100 nanosegundos.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **un valor LONGLONG.**

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Si el objeto que crea la secuencia de bytes puede determinar la duración, puede establecer este atributo. (Por ejemplo, en un flujo de red, la duración puede formar parte de la descripción de la sesión).

Para obtener el valor del atributo, llame a **QueryInterface** en la secuencia de bytes para obtener un puntero a la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Este atributo es un valor con firma, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de flujo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




