---
title: Evento external. OnSendMessageComplete
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Media Player de eventos external. OnSendMessageComplete de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698589"
---
# <a name="externalonsendmessagecomplete-event"></a>Evento external. OnSendMessageComplete

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El evento **OnSendMessageComplete** se produce cuando la tienda en línea ha finalizado el procesamiento de un mensaje. El script de la página de detección envió previamente el mensaje mediante una llamada a [external. SendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento tiene los parámetros siguientes.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Mensaje*
</dt> <dd>

La misma cadena que se pasó en el parámetro **MSG** de **SendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

La misma cadena que se pasó en el parámetro **param** de **SendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Da*
</dt> <dd>

**Cadena** que contiene el resultado del control de mensajes. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método **SendMessage** llama a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), que devuelve de forma asincrónica. Es decir, se devuelve antes de que la tienda en línea termine de procesar el mensaje. Cuando la tienda en línea termina de procesar el mensaje, llama a [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), que a su vez llama al controlador de eventos **OnSendMessageComplete** del script.

Cuando la tienda en línea llama a **IWMPContentPartnerCallback:: SendMessageComplete**, proporciona un código de resultado en el parámetro *bstrResult* . Windows Media Player no interpreta ese código de resultado. En su lugar, Windows Media Player pasa el código de resultado junto con el controlador de eventos **OnSendMessageComplete** en el parámetro *result* .

Windows Media Player interpreta ninguno de los parámetros (*MSG*, *param*, *result*) del controlador de eventos **OnSendMessageComplete** . Los parámetros solo tienen significado en la tienda en línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





