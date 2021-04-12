---
description: Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'IWinHttpRequest:: SetClientCertificate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361040"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>IWinHttpRequest:: SetClientCertificate (método)

El método **SetClientCertificate** selecciona un certificado de cliente para enviarlo a un servidor de protocolo seguro de transferencia de hipertexto (https).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientCertificate* \[ de\]
</dt> <dd>

Especifica la ubicación, el [*almacén de certificados*](glossary.md)y el asunto de un certificado de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

La cadena especificada en el parámetro *ClientCertificate* consta de la ubicación del certificado, el almacén de certificados y el nombre de sujeto delimitados por barras diagonales inversas. Para obtener más información acerca de los componentes de la cadena de certificado, consulte [certificados de cliente](ssl-in-winhttp.md).

El nombre y la ubicación del almacén de certificados son opcionales. Sin embargo, si especifica un almacén de certificados, también debe especificar la ubicación del almacén de certificados. La ubicación predeterminada es \_ usuario actual y el almacén de certificados predeterminado es "My". Un asunto en blanco indica que se debe usar el primer certificado del almacén de certificados.

Llame a **SetClientCertificate** para seleccionar un certificado antes de llamar a [**send**](iwinhttprequest-send.md) para enviar la solicitud.

Los servicios HTTP de Microsoft Windows (WinHTTP) no proporcionan certificados de cliente a los servidores proxy que solicitan certificados para la autenticación.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de scripting siguiente se muestra cómo seleccionar un certificado de cliente para enviarlo con una solicitud. Se elige un certificado con el asunto "My Middle-Tier Certificate" en el almacén de certificados "personal" del registro en **HKEY \_ local \_ Machine**. Dado que este ejemplo de código es específico de Microsoft JScript, que usa la barra diagonal inversa como carácter de escape, se requieren dos barras diagonales inversas adyacentes para delimitar los componentes de la cadena de certificado.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



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

[SSL en WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




