---
title: Evento External.OnSendMessageComplete
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Evento External.OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Evento External.OnSendMessageComplete Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241892"
---
# <a name="externalonsendmessagecomplete-event"></a>Evento External.OnSendMessageComplete

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **evento OnSendMessageComplete** tiene lugar cuando la tienda en línea ha terminado de procesar un mensaje. El script de la página de detección envió previamente el mensaje mediante una llamada [a External.sendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Se trata de una propiedad de solo escritura que especifica el nombre de la función en el script que Reproductor de Windows Media llama cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento tiene los parámetros siguientes.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*
</dt> <dd>

La misma cadena que se pasó en el parámetro **Msg** de **sendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

La misma cadena que se pasó en el parámetro **Param** de **sendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Resultado*
</dt> <dd>

**Cadena** que contiene el resultado del control de mensajes. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **método sendMessage** llama [a IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), que devuelve de forma asincrónica. Es decir, devuelve antes de que la tienda en línea termine de procesar el mensaje. Cuando el almacén en línea termina de procesar el mensaje, llama a [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), que a su vez llama al controlador de eventos **OnSendMessageComplete del** script.

Cuando el almacén en línea llama a **IWMPContentPartnerCallback::SendMessageComplete**, proporciona un código de resultado en el *parámetro bstrResult.* Reproductor de Windows Media no interpreta ese código de resultado. En su lugar, Reproductor de Windows Media el código de resultado junto con el controlador de eventos **OnSendMessageComplete** en el *parámetro Result.*

Ninguno de los parámetros (*Msg*, *Param*, *Result*) del controlador de eventos **OnSendMessageComplete** se interpreta Reproductor de Windows Media. Los parámetros solo tienen significado para la tienda en línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





