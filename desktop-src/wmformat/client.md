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
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="75699-111">Registro de cliente (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="75699-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="75699-112">Cuando el objeto lector lee datos de un servidor, envía información de registro al servidor.</span><span class="sxs-lookup"><span data-stu-id="75699-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="75699-113">Los proveedores de contenido suelen usar esta información para medir la calidad del servicio, generar información de facturación o realizar un seguimiento de la publicidad.</span><span class="sxs-lookup"><span data-stu-id="75699-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="75699-114">La información de registro no contiene datos personales.</span><span class="sxs-lookup"><span data-stu-id="75699-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="75699-115">La aplicación puede especificar parte de la información que se registra, llamando al método [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) en el objeto del lector.</span><span class="sxs-lookup"><span data-stu-id="75699-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="75699-116">Por ejemplo, puede especificar la cadena de agente de usuario, el nombre de la aplicación de reproducción o la página web que hospeda el reproductor.</span><span class="sxs-lookup"><span data-stu-id="75699-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="75699-117">La información de registro incluye un GUID que identifica la sesión.</span><span class="sxs-lookup"><span data-stu-id="75699-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="75699-118">De forma predeterminada, el lector genera un identificador de sesión anónimo.</span><span class="sxs-lookup"><span data-stu-id="75699-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="75699-119">Opcionalmente, el lector puede enviar en su lugar un identificador que identifica de forma única al usuario actual.</span><span class="sxs-lookup"><span data-stu-id="75699-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="75699-120">Para habilitar esta característica, llame al método [**IWMReaderAdvanced2:: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="75699-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="75699-121">Puede configurar el objeto lector para enviar la información de registro a otro servidor, además del servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="75699-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="75699-122">Para ello, llame al método [**IWMReaderNetworkConfig:: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con la dirección URL del servidor.</span><span class="sxs-lookup"><span data-stu-id="75699-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="75699-123">Esta dirección URL debe apuntar a un script o ejecutable que pueda controlar las solicitudes GET y POST de HTTP.</span><span class="sxs-lookup"><span data-stu-id="75699-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="75699-124">Puede usar el agente de anuncios de multidifusión y registro (wmsiislog.dll), o puede escribir un script ASP o CGI personalizado para recibir los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="75699-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="75699-125">Puede obtener la misma funcionalidad si crea una lista de reproducción del servidor con un atributo **logURL** .</span><span class="sxs-lookup"><span data-stu-id="75699-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="75699-126">Cuando el objeto lector envía el registro, hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="75699-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="75699-127">Envía una solicitud GET vacía al servidor.</span><span class="sxs-lookup"><span data-stu-id="75699-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="75699-128">Analiza la respuesta del servidor para una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="75699-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="75699-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` donde "0.0.0.0" es un número de versión válido.</span><span class="sxs-lookup"><span data-stu-id="75699-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="75699-130">Envía una solicitud POST con la información de registro.</span><span class="sxs-lookup"><span data-stu-id="75699-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="75699-131">En el código siguiente se muestra un script ASP de ejemplo que recibe la información de registro y la escribe en un archivo:</span><span class="sxs-lookup"><span data-stu-id="75699-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


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



<span data-ttu-id="75699-132">Puede especificar varios servidores para recibir información de registro; simplemente llame a **AddLoggingUrl** una vez con cada dirección URL.</span><span class="sxs-lookup"><span data-stu-id="75699-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="75699-133">Para borrar la lista de servidores que reciben registros, llame al método [**IWMReaderNetworkConfig:: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .</span><span class="sxs-lookup"><span data-stu-id="75699-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75699-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75699-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75699-135">**Implementación de la funcionalidad de red**</span><span class="sxs-lookup"><span data-stu-id="75699-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="75699-136">**Interfaz IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="75699-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="75699-137">**Interfaz IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="75699-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




