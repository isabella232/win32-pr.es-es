---
description: Especifica si una transformación de Media Foundation basada en hardware (MFT) está conectada a otra MFT basada en hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602875"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>Atributo MFT \_ CONNECTED \_ TO HW \_ \_ STREAM

Especifica si una transformación de Media Foundation basada en hardware (MFT) está conectada a otra MFT basada en hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Normalmente, las aplicaciones no usan este atributo.

Este atributo se usa con MTA basados en hardware. Cuando dos MTA de hardware están conectados dentro de una topología, el cargador de topologías establece este atributo en **TRUE** en los objetos siguientes:

-   El flujo de salida del MFT ascendente
-   Flujo de entrada del MFT de bajada

Para obtener el almacén de atributos para el flujo de salida, el cargador de topologías llama [**a IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) en el MFT ascendente. Para obtener el almacén de atributos para el flujo de entrada, el cargador de topología llama [**a IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) en el MFT de bajada.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MTA de hardware](hardware-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




