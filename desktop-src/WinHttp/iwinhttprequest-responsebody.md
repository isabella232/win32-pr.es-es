---
description: Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'IWinHttpRequest:: ResponseBody (propiedad)'
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
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707220"
---
# <a name="iwinhttprequestresponsebody-property"></a>IWinHttpRequest:: ResponseBody (propiedad)

La propiedad **ResponseBody** recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.

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

Un valor **Variant** que recibe el cuerpo de la entidad de respuesta como una matriz de bytes sin signo. Esta matriz contiene los datos sin procesar recibidos directamente desde el servidor.

## <a name="error-codes"></a>Códigos de error

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve los datos de la respuesta en una matriz de bytes sin signo. Si la respuesta no tiene un cuerpo de respuesta, se devuelve una variante vacía. Esta propiedad solo se puede invocar después de que se haya llamado al método [**send**](iwinhttprequest-send.md) .

> [!Note]  
> Para obtener más información acerca de la implementación de Windows XP y Windows 2000, consulte [requisitos de tiempo de ejecución](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




