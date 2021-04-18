---
description: 'Contiene un puntero al token que se proporcionó al método IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: MFSampleExtension_Token atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720444"
---
# <a name="mfsampleextension_token-attribute"></a>Atributo de token de MFSampleExtension \_

Contiene un puntero al token que se proporcionó al método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los ejemplos de medios. El valor del atributo es el puntero **IUnknown** que se pasa al parámetro *PToken* del método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . El autor de la llamada utiliza este atributo para realizar el seguimiento del estado de la solicitud.

Si está escribiendo un origen multimedia personalizado, establezca este atributo en el ejemplo cuando el flujo multimedia entregue un ejemplo en respuesta al método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a menos que el valor de *pToken* sea **null**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> </dl>

 

 




