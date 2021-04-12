---
title: Registro de cliente (Windows Media Format 11 SDK)
description: Registro de cliente
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- SDK de Windows Media Format, registro de cliente
- SDK de Windows Media Format, registro
- Advanced Systems Format (ASF), registro de cliente
- ASF (formato de sistemas avanzados), registro de cliente
- Advanced Systems Format (ASF), registro
- ASF (formato de sistemas avanzados), registro
- registro de cliente
- clientes de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149768"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Registro de cliente (Windows Media Format 11 SDK)

Cuando el objeto lector lee datos de un servidor, envía información de registro al servidor. Los proveedores de contenido suelen usar esta información para medir la calidad del servicio, generar información de facturación o realizar un seguimiento de la publicidad. La información de registro no contiene datos personales.

La aplicación puede especificar parte de la información que se registra, llamando al método [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) en el objeto del lector. Por ejemplo, puede especificar la cadena de agente de usuario, el nombre de la aplicación de reproducción o la página web que hospeda el reproductor.

La información de registro incluye un GUID que identifica la sesión. De forma predeterminada, el lector genera un identificador de sesión anónimo. Opcionalmente, el lector puede enviar en su lugar un identificador que identifica de forma única al usuario actual. Para habilitar esta característica, llame al método [**IWMReaderAdvanced2:: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con el valor **true**.

Puede configurar el objeto lector para enviar la información de registro a otro servidor, además del servidor de origen. Para ello, llame al método [**IWMReaderNetworkConfig:: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con la dirección URL del servidor. Esta dirección URL debe apuntar a un script o ejecutable que pueda controlar las solicitudes GET y POST de HTTP. Puede usar el agente de anuncios de multidifusión y registro (wmsiislog.dll), o puede escribir un script ASP o CGI personalizado para recibir los datos de registro.

> [!Note]  
> Puede obtener la misma funcionalidad si crea una lista de reproducción del servidor con un atributo **logURL** .

 

Cuando el objeto lector envía el registro, hace lo siguiente:

1.  Envía una solicitud GET vacía al servidor.
2.  Analiza la respuesta del servidor para una de las siguientes cadenas:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` donde "0.0.0.0" es un número de versión válido.
3.  Envía una solicitud POST con la información de registro.

En el código siguiente se muestra un script ASP de ejemplo que recibe la información de registro y la escribe en un archivo:


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



Puede especificar varios servidores para recibir información de registro; simplemente llame a **AddLoggingUrl** una vez con cada dirección URL. Para borrar la lista de servidores que reciben registros, llame al método [**IWMReaderNetworkConfig:: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> <dt>

[**Interfaz IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**Interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




