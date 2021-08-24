---
title: Método External.sendMessage
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método sendMessage envía un mensaje al complemento de la tienda en línea.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- Método sendMessage Reproductor de Windows Media
- Método sendMessage Reproductor de Windows Media , clase External
- Clase externa Reproductor de Windows Media , método sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648374"
---
# <a name="externalsendmessage-method"></a>Método External.sendMessage

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método sendMessage** envía un mensaje al complemento de la tienda en línea.

## <a name="syntax"></a>Sintaxis


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Mensaje* \[ En\]
</dt> <dd>

**Cadena** que contiene el mensaje.

</dd> <dt>

*Param* \[ En\]
</dt> <dd>

**Cadena** que contiene parámetros asociados al mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El mensaje se envía de forma asincrónica. Es decir, este método devuelve inmediatamente en lugar de esperar a que se procese el mensaje. Cuando el complemento termina de procesar el mensaje, llama al método [IWMPContentPartnerCallback::SendMessageComplete,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) que a su vez llama al controlador de eventos [OnSendMessageComplete](external-onsendmessagecomplete-event.md) del script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





