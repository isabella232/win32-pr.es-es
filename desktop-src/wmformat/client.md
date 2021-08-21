---
title: Registro de cliente (Windows SDK de formato multimedia 11)
description: Obtenga información sobre el registro de cliente Windows SDK de Formato multimedia 11. El registro proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows SDK de formato multimedia, registro de cliente
- Windows SDK de formato multimedia, registro
- Formato de sistemas avanzados (ASF), registro de cliente
- ASF (formato de sistemas avanzados), registro de cliente
- Formato de sistemas avanzados (ASF), registro
- ASF (formato de sistemas avanzados), registro
- registro de cliente
- registrar clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460058d6ad4009fab301c6ce322df3144bdd0e5d9bb4732d54126f7675cd9e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028033"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>Registro de cliente (Windows SDK de formato multimedia 11)

Cuando el objeto de lector lee datos de un servidor, envía información de registro al servidor. Normalmente, los proveedores de contenido usan esta información para medir la calidad del servicio, generar información de facturación o realizar un seguimiento de la publicidad. La información de registro no contiene datos personales.

La aplicación puede especificar parte de la información que se registra mediante una llamada al método [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) en el objeto reader. Por ejemplo, puede especificar la cadena de agente de usuario, el nombre de la aplicación del reproductor o la página web que hospeda el reproductor.

La información de registro incluye un GUID que identifica la sesión. De forma predeterminada, el lector genera un identificador de sesión anónimo. Opcionalmente, el lector puede enviar en su lugar un identificador que identifique de forma única al usuario actual. Para habilitar esta característica, llame al método [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con el valor **TRUE**.

Puede configurar el objeto de lector para enviar la información de registro a otro servidor, además del servidor de origen. Para ello, llame al [**método IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con la dirección URL del servidor. Esta dirección URL debe apuntar a un script o ejecutable que pueda controlar las solicitudes HTTP GET y POST. Puede usar el Agente de anuncios de multidifusión y registro (wmsiislog.dll), o bien puede escribir un script personalizado de ASP o CGI para recibir los datos de registro.

> [!Note]  
> Puede obtener la misma funcionalidad mediante la creación de una lista de reproducción del lado servidor con un **atributo logURL.**

 

Cuando el objeto reader envía el registro, hace lo siguiente:

1.  Envía una solicitud GET vacía al servidor.
2.  Analiza la respuesta del servidor para una de las cadenas siguientes:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` donde "0.0.0.0" es cualquier número de versión válido.
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



Puede especificar varios servidores para recibir información de registro; Simplemente llame a **AddLoggingUrl una** vez con cada dirección URL. Para borrar la lista de servidores que reciben registros, llame al [**método IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> <dt>

[**IWMReaderAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**IWMReaderAdvanced2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




