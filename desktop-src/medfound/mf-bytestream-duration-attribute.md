---
description: Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360516"
---
# <a name="mf_bytestream_duration-attribute"></a>\_Atributo de \_ duración MF BYTESTREAM

Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Si el objeto que crea el flujo de bytes puede determinar la duración, puede establecer este atributo. (Por ejemplo, en un flujo de red, la duración puede ser parte de la descripción de la sesión).

Para obtener el valor del atributo, llame a **QueryInterface** en el flujo de bytes para obtener un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Este atributo es un valor con signo, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de secuencia de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




