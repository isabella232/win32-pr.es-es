---
description: Contiene un puntero al token que se proporcionó al método IMFMediaStream::RequestSample.
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: MFSampleExtension_Token atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8efcf176c20e9cd4ce24528146797398918907d16d772539614692b9d53b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872334"
---
# <a name="mfsampleextension_token-attribute"></a>Atributo de token MFSampleExtension \_

Contiene un puntero al token que se proporcionó al [**método IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los ejemplos multimedia. El valor del atributo es el **puntero IUnknown** que se pasa al *parámetro pToken* del [**método RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) El autor de la llamada usa este atributo para realizar un seguimiento del estado de la solicitud.

Si está escribiendo un origen multimedia personalizado, establezca este atributo en el ejemplo cuando el flujo multimedia entregue un ejemplo en respuesta al método [**RequestSample,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) a menos que el valor de *pToken* sea **NULL.**

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
</dt> </dl>

 

 




