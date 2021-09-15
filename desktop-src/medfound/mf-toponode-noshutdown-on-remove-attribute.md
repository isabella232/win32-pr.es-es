---
description: Especifica cómo la sesión multimedia cierra un objeto en la topología.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: MF_TOPONODE_NOSHUTDOWN_ON_REMOVE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb7db9a883db80cc6154c72d2c4218b7815456b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468675"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>Atributo MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE

Especifica cómo la sesión multimedia cierra un objeto en la topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los siguientes tipos de nodo de topología:

-   Nodos de salida
-   Cualquier nodo de transformación que contenga una *transformación* Media Foundation transformación asincrónica (MFT).

El atributo puede tener los siguientes valores:




| Value | Descripción | 
|-------|-------------|
| <strong>TRUE</strong> | Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, no apaga el objeto que pertenece a este nodo de topología. | 
| <strong>FALSE</strong> | Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, apaga el objeto de nodo, como se muestra a continuación:<ul><li>Nodos de salida: la sesión llama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>a IMFMediaSink::Shutdown</strong></a> en el receptor de medios.</li><li>Transformar nodos: la sesión llama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>a IMFShutdown::Shutdown</strong></a> en MFT.</li></ul> | 




 

El valor predeterminado es **TRUE.**

Si la aplicación pone en cola varias topologías, es una buena idea establecer este atributo en **FALSE.** De lo contrario, es posible que los objetos de la topología no se apaguen correctamente.

Este atributo no se aplica cuando la aplicación cierra la sesión multimedia mediante una llamada [**a IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Cuando se cierra la sesión multimedia, siempre apaga los receptores multimedia y los MTA asincrónicos en la topología actual.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




