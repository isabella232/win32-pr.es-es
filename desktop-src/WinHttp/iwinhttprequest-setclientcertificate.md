---
description: Selecciona un certificado de cliente que se enviará a un servidor https (Protocolo seguro de transferencia de hipertexto).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: IWinHttpRequest::SetClientCertificate (método)
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
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562901"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>IWinHttpRequest::SetClientCertificate (método)

El **método SetClientCertificate** selecciona un certificado de cliente para enviarlo a un servidor https (Protocolo seguro de transferencia de hipertexto).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientCertificate* \[ En\]
</dt> <dd>

Especifica la ubicación, el [*almacén de certificados*](glossary.md)y el asunto de un certificado de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK on** success o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

La cadena especificada en el parámetro *ClientCertificate* consta de la ubicación del certificado, el almacén de certificados y el nombre del sujeto delimitados por barras diagonales inversas. Para obtener más información sobre los componentes de la cadena de certificado, vea [Certificados de cliente](ssl-in-winhttp.md).

El nombre y la ubicación del almacén de certificados son opcionales. Sin embargo, si especifica un almacén de certificados, también debe especificar la ubicación de ese almacén de certificados. La ubicación predeterminada es CURRENT \_ USER y el almacén de certificados predeterminado es "MY". Un asunto en blanco indica que se debe usar el primer certificado del almacén de certificados.

Llame **a SetClientCertificate** para seleccionar un certificado antes de llamar a [**Send**](iwinhttprequest-send.md) para enviar la solicitud.

Microsoft Windows HTTP Services (WinHTTP) no proporciona certificados de cliente a los servidores proxy que solicitan certificados para la autenticación.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de scripting siguiente se muestra cómo seleccionar un certificado de cliente para enviar con una solicitud. Se elige un certificado con el asunto "Mi Middle-Tier certificado" del almacén de certificados "Personal" en el Registro en **HKEY \_ LOCAL \_ MACHINE**. Dado que este ejemplo de código es específico de Microsoft JScript, que usa la barra diagonal inversa como carácter de escape, se necesitan dos barras diagonales inversas adyacentes para delimitar los componentes de la cadena de certificado.


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
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
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

 

 




