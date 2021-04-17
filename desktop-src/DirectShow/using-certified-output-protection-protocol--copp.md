---
description: Uso del Protocolo de protección de la salida certificada (COPP)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Uso del Protocolo de protección de la salida certificada (COPP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678085"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="7af9b-103">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="7af9b-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="7af9b-104">El protocolo de protección de la salida certificada (COPP) permite a una aplicación proteger una secuencia de vídeo mientras se desplaza desde el adaptador de gráficos al dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="7af9b-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="7af9b-105">Una aplicación puede usar COPP para detectar qué tipo de conector físico está conectado al dispositivo de pantalla y qué tipos de protección de salida están disponibles.</span><span class="sxs-lookup"><span data-stu-id="7af9b-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="7af9b-106">Entre los mecanismos de protección se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7af9b-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="7af9b-107">High-Bandwidth Digital Content Protection (HDCP)</span><span class="sxs-lookup"><span data-stu-id="7af9b-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="7af9b-108">Sistema de administración de generación de copias: analógico (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="7af9b-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="7af9b-109">Protección de copia analógica (ACP)</span><span class="sxs-lookup"><span data-stu-id="7af9b-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="7af9b-110">Si el adaptador de gráficos admite uno de estos mecanismos, la aplicación puede usar COPP para establecer el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="7af9b-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="7af9b-111">COPP define un protocolo que se usa para establecer un canal de comunicaciones seguro con el controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="7af9b-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="7af9b-112">Usa códigos de autenticación de mensajes (Mac) para comprobar la integridad de los comandos COPP que se pasan entre la aplicación y el controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="7af9b-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="7af9b-113">La aplicación usa COPP llamando a los métodos de la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) del filtro de representador de combinación de vídeo de DIRECTSHOW (VMR-7 o VMR-9).</span><span class="sxs-lookup"><span data-stu-id="7af9b-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="7af9b-114">COPP no define nada sobre las directivas de derechos digitales que se pueden aplicar a contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="7af9b-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="7af9b-115">Además, el propio COPP no implementa ningún sistema de protección de salida.</span><span class="sxs-lookup"><span data-stu-id="7af9b-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="7af9b-116">El protocolo COPP simplemente proporciona una manera de establecer y consultar los niveles de protección en el adaptador de gráficos mediante los sistemas de protección que proporciona el adaptador.</span><span class="sxs-lookup"><span data-stu-id="7af9b-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="7af9b-117">En esta sección se da por supuesto que está familiarizado con las siguientes tecnologías:</span><span class="sxs-lookup"><span data-stu-id="7af9b-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="7af9b-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="7af9b-118">DirectShow</span></span>
-   <span data-ttu-id="7af9b-119">SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="7af9b-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="7af9b-120">XML</span><span class="sxs-lookup"><span data-stu-id="7af9b-120">XML</span></span>
-   <span data-ttu-id="7af9b-121">Criptografía de clave pública y criptografía simétrica</span><span class="sxs-lookup"><span data-stu-id="7af9b-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="7af9b-122">Los ejemplos de código de esta sección usan CryptoAPI de Microsoft para realizar operaciones criptográficas.</span><span class="sxs-lookup"><span data-stu-id="7af9b-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="7af9b-123">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="7af9b-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="7af9b-124">Información general de COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="7af9b-125">Obtención de la cadena de certificados del controlador</span><span class="sxs-lookup"><span data-stu-id="7af9b-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="7af9b-126">Validar la cadena de certificados</span><span class="sxs-lookup"><span data-stu-id="7af9b-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="7af9b-127">Listas de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="7af9b-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="7af9b-128">Importar la clave pública del controlador</span><span class="sxs-lookup"><span data-stu-id="7af9b-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="7af9b-129">Iniciar una sesión de COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="7af9b-130">Envío de solicitudes de estado de COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="7af9b-131">Envío de comandos COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="7af9b-132">Prueba de si un controlador de gráficos es compatible con COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="7af9b-133">Referencia de consulta de COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="7af9b-134">Referencia de comandos de COPP</span><span class="sxs-lookup"><span data-stu-id="7af9b-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="7af9b-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7af9b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7af9b-136">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="7af9b-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



