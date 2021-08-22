---
description: Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: IWinHttpRequest::ResponseBody, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563233"
---
# <a name="iwinhttprequestresponsebody-property"></a>IWinHttpRequest::ResponseBody, propiedad

La **propiedad ResponseBody** recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Valor de propiedad

Valor **Variant** que recibe el cuerpo de la entidad de respuesta como una matriz de bytes sin signo. Esta matriz contiene los datos sin procesar recibidos directamente del servidor.

## <a name="error-codes"></a>Códigos de error

El valor devuelto es **S \_ OK si se** ejecuta correctamente o un valor de error en caso contrario.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve los datos de respuesta en una matriz de bytes sin signo. Si la respuesta no tiene un cuerpo de respuesta, se devuelve una variante vacía. Esta propiedad solo se puede invocar después [**de**](iwinhttprequest-send.md) llamar al método Send.

> [!Note]  
> Para obtener más información sobre la implementación de Windows XP y Windows 2000, vea [Requisitos en tiempo de ejecución](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




