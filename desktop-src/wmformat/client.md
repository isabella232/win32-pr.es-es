---
title: Registro de cliente (Windows Media Format SDK 11)
description: Obtenga información sobre el registro de cliente Windows Media Format SDK 11. El registro proporciona una manera de que el servidor multimedia realice un seguimiento de la actividad de los clientes que se conectan a él.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK,registro de cliente
- Windows Media Format SDK, registro
- Formato de sistemas avanzados (ASF), registro de cliente
- ASF (formato de sistemas avanzados), registro de cliente
- Formato de sistemas avanzados (ASF), registro
- ASF (formato de sistemas avanzados), registro
- registro de cliente
- registrar clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406268"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="d7522-112">Registro de cliente (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="d7522-112">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d7522-113">Cuando el objeto de lector lee datos de un servidor, envía información de registro al servidor.</span><span class="sxs-lookup"><span data-stu-id="d7522-113">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="d7522-114">Normalmente, los proveedores de contenido usan esta información para medir la calidad del servicio, generar información de facturación o realizar un seguimiento de la publicidad.</span><span class="sxs-lookup"><span data-stu-id="d7522-114">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="d7522-115">La información de registro no contiene datos personales.</span><span class="sxs-lookup"><span data-stu-id="d7522-115">The logging information contains no personal data.</span></span>

<span data-ttu-id="d7522-116">La aplicación puede especificar parte de la información que se registra mediante una llamada al método [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) en el objeto reader.</span><span class="sxs-lookup"><span data-stu-id="d7522-116">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="d7522-117">Por ejemplo, puede especificar la cadena de agente de usuario, el nombre de la aplicación del reproductor o la página web que hospeda el reproductor.</span><span class="sxs-lookup"><span data-stu-id="d7522-117">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="d7522-118">La información de registro incluye un GUID que identifica la sesión.</span><span class="sxs-lookup"><span data-stu-id="d7522-118">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="d7522-119">De forma predeterminada, el lector genera un identificador de sesión anónimo.</span><span class="sxs-lookup"><span data-stu-id="d7522-119">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="d7522-120">Opcionalmente, el lector puede enviar en su lugar un identificador que identifique de forma única al usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d7522-120">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="d7522-121">Para habilitar esta característica, llame al método [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con el valor **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="d7522-121">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="d7522-122">Puede configurar el objeto de lector para enviar la información de registro a otro servidor, además del servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="d7522-122">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="d7522-123">Para ello, llame al [**método IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con la dirección URL del servidor.</span><span class="sxs-lookup"><span data-stu-id="d7522-123">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="d7522-124">Esta dirección URL debe apuntar a un script o ejecutable que pueda controlar las solicitudes HTTP GET y POST.</span><span class="sxs-lookup"><span data-stu-id="d7522-124">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="d7522-125">Puede usar el Agente de anuncios de multidifusión y registro (wmsiislog.dll), o bien puede escribir un script personalizado de ASP o CGI para recibir los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="d7522-125">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="d7522-126">Puede obtener la misma funcionalidad mediante la creación de una lista de reproducción del lado servidor con un **atributo logURL.**</span><span class="sxs-lookup"><span data-stu-id="d7522-126">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="d7522-127">Cuando el objeto reader envía el registro, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d7522-127">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="d7522-128">Envía una solicitud GET vacía al servidor.</span><span class="sxs-lookup"><span data-stu-id="d7522-128">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="d7522-129">Analiza la respuesta del servidor para una de las cadenas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7522-129">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="d7522-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` donde "0.0.0.0" es cualquier número de versión válido.</span><span class="sxs-lookup"><span data-stu-id="d7522-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="d7522-131">Envía una solicitud POST con la información de registro.</span><span class="sxs-lookup"><span data-stu-id="d7522-131">Sends a POST request with the log information.</span></span>

<span data-ttu-id="d7522-132">En el código siguiente se muestra un script ASP de ejemplo que recibe la información de registro y la escribe en un archivo:</span><span class="sxs-lookup"><span data-stu-id="d7522-132">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


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



<span data-ttu-id="d7522-133">Puede especificar varios servidores para recibir información de registro; Simplemente llame a **AddLoggingUrl una** vez con cada dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d7522-133">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="d7522-134">Para borrar la lista de servidores que reciben registros, llame al [**método IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)</span><span class="sxs-lookup"><span data-stu-id="d7522-134">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7522-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7522-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7522-136">**Implementación de la funcionalidad de red**</span><span class="sxs-lookup"><span data-stu-id="d7522-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="d7522-137">**IWMReaderAdvanced (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d7522-137">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="d7522-138">**IWMReaderAdvanced2 (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d7522-138">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




