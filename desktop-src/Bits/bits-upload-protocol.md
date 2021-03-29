---
title: Protocolo de carga de BITS
description: En esta sección se describe el protocolo de red para los tipos de trabajo carga de BITS y carga-respuesta.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773680"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="481d4-103">Protocolo de carga de BITS</span><span class="sxs-lookup"><span data-stu-id="481d4-103">BITS Upload Protocol</span></span>

<span data-ttu-id="481d4-104">En esta sección se describe el protocolo de red para los tipos de trabajo carga de BITS y carga-respuesta.</span><span class="sxs-lookup"><span data-stu-id="481d4-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="481d4-105">El protocolo de carga de BITS está superpuesto a HTTP 1,1 y utiliza muchos de los encabezados HTTP existentes y define nuevos encabezados.</span><span class="sxs-lookup"><span data-stu-id="481d4-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="481d4-106">El protocolo de carga de BITS admite un solo archivo de carga por sesión.</span><span class="sxs-lookup"><span data-stu-id="481d4-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="481d4-107">BITS usa paquetes para describir las solicitudes de cliente y las respuestas del servidor.</span><span class="sxs-lookup"><span data-stu-id="481d4-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="481d4-108">El encabezado BITS-paquete-tipo especifica el tipo de paquete que se envía.</span><span class="sxs-lookup"><span data-stu-id="481d4-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="481d4-109">Cada paquete contiene encabezados concretos.</span><span class="sxs-lookup"><span data-stu-id="481d4-109">Each packet contains specific headers.</span></span> <span data-ttu-id="481d4-110">BITS utiliza el \_ verbo post de bits para identificar los paquetes de carga de bits.</span><span class="sxs-lookup"><span data-stu-id="481d4-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="481d4-111">Los paquetes de respuesta siempre usan el tipo de paquete ACK que representa la confirmación.</span><span class="sxs-lookup"><span data-stu-id="481d4-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="481d4-112">El paquete de confirmación se envía en el contexto de la solicitud anterior; solo puede haber una solicitud pendiente al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="481d4-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="481d4-113">En el caso de los trabajos de carga y respuesta, BITS usa este protocolo para cargar el archivo, pero no usa este protocolo para enviar la respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="481d4-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="481d4-114">En su lugar, el servidor BITS envía la ubicación del archivo de respuesta al cliente y el cliente crea un trabajo de descarga de BITS para descargar el archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="481d4-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="481d4-115">Use el protocolo de carga para reemplazar el software de cliente o servidor de BITS por su propia implementación.</span><span class="sxs-lookup"><span data-stu-id="481d4-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="481d4-116">Para obtener una lista de los paquetes de solicitud enviados por el cliente BITS, consulte [paquetes de solicitud de bits](bits-request-packets.md).</span><span class="sxs-lookup"><span data-stu-id="481d4-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="481d4-117">Para obtener una lista de los paquetes de respuesta enviados por el servidor BITS, consulte [paquetes de respuesta de bits](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="481d4-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="481d4-118">El cliente determina el modo en que responde a errores o paquetes inesperados del servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="481d4-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="481d4-119">Si el servidor recibe un paquete que no espera, el servidor debe enviar un paquete de confirmación con un código de retorno 400 (solicitud incorrecta).</span><span class="sxs-lookup"><span data-stu-id="481d4-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




