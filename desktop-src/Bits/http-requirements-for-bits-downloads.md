---
title: Requisitos HTTP para descargas de BITS
description: BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486646"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="7bf87-103">Requisitos HTTP para descargas de BITS</span><span class="sxs-lookup"><span data-stu-id="7bf87-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="7bf87-104">BITS admite descargas y cargas HTTP y HTTPS, y requiere que el servidor admita el protocolo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="7bf87-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="7bf87-105">En el caso de las descargas, el método **principal** del servidor http debe devolver el tamaño del archivo y su método **Get** debe admitir los encabezados Content-Range y Content-Length.</span><span class="sxs-lookup"><span data-stu-id="7bf87-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="7bf87-106">Como resultado, BITS solo transfiere el contenido del archivo estático y genera un error si se intenta transferir contenido dinámico, a menos que el script ASP, ISAPI o CGI admita los encabezados Content-Range y Content-Length.</span><span class="sxs-lookup"><span data-stu-id="7bf87-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="7bf87-107">BITS puede usar un servidor HTTP/1.0 siempre que cumpla los requisitos de los métodos **Head** y **Get** .</span><span class="sxs-lookup"><span data-stu-id="7bf87-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="7bf87-108">Para admitir la descarga de intervalos de un archivo, el servidor debe admitir los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="7bf87-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="7bf87-109">Permita que los encabezados MIME incluyan los encabezados Content-Range y Content-Type estándar, además de un máximo de 180 bytes de otros encabezados.</span><span class="sxs-lookup"><span data-stu-id="7bf87-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="7bf87-110">Permite un máximo de dos CR/LFs entre los encabezados HTTP y la primera cadena de límite.</span><span class="sxs-lookup"><span data-stu-id="7bf87-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




