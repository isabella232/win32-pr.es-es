---
title: External. sendMessage (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método sendMessage envía un mensaje al complemento de la tienda en línea.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- método sendMessage de Windows Media Player
- método sendMessage Windows Media Player, clase externa
- Clase externa Windows Media Player, método sendMessage
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
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699727"
---
# <a name="externalsendmessage-method"></a>External. sendMessage (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **SendMessage** envía un mensaje al complemento de la tienda en línea.

## <a name="syntax"></a>Sintaxis


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Mensaje* \[ de de\]
</dt> <dd>

**Cadena** que contiene el mensaje.

</dd> <dt>

*Parámetro* \[ de\]
</dt> <dd>

**Cadena** que contiene los parámetros asociados al mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje se envía de forma asincrónica. Es decir, este método vuelve inmediatamente en lugar de esperar a que se procese el mensaje. Cuando el complemento termina de procesar el mensaje, llama al método [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , que a su vez llama al controlador de eventos [OnSendMessageComplete](external-onsendmessagecomplete-event.md) del script.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





