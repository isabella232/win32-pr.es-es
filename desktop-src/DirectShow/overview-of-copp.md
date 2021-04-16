---
description: Información general de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Información general de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686335"
---
# <a name="overview-of-copp"></a><span data-ttu-id="8942e-103">Información general de COPP</span><span class="sxs-lookup"><span data-stu-id="8942e-103">Overview of COPP</span></span>

<span data-ttu-id="8942e-104">Estos son los pasos básicos que una aplicación debe realizar para usar el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="8942e-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="8942e-105">**Obtención de la cadena de certificados del controlador**</span><span class="sxs-lookup"><span data-stu-id="8942e-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="8942e-106">Cree un gráfico de reproducción de DirectShow que represente vídeo con el representador de mezcla de vídeo (VMR-7 o VMR-9) o el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="8942e-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="8942e-107">Consulte el VMR para la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .</span><span class="sxs-lookup"><span data-stu-id="8942e-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="8942e-108">Llame a [**IAMCertifiedOutputProtection:: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="8942e-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="8942e-109">Este método devuelve un número aleatorio de 128 bits del controlador, junto con una cadena de certificados que contiene la clave pública RSA de 2048 bits del controlador.</span><span class="sxs-lookup"><span data-stu-id="8942e-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="8942e-110">**Validar la cadena de certificados**</span><span class="sxs-lookup"><span data-stu-id="8942e-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="8942e-111">Validar la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="8942e-111">Validate the certificate chain.</span></span> <span data-ttu-id="8942e-112">Si la cadena de certificados no es válida, detenga.</span><span class="sxs-lookup"><span data-stu-id="8942e-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="8942e-113">Compruebe la lista de revocación de certificados (CRL).</span><span class="sxs-lookup"><span data-stu-id="8942e-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="8942e-114">Si alguno de los certificados de la cadena de certificados aparece en la lista de revocación, detenga.</span><span class="sxs-lookup"><span data-stu-id="8942e-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="8942e-115">Obtiene la clave pública RSA de la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="8942e-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="8942e-116">**Inicializar la sesión COPP**</span><span class="sxs-lookup"><span data-stu-id="8942e-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="8942e-117">Genere una clave de sesión AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="8942e-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="8942e-118">Esta clave se usa para firmar datos y para comprobar que los datos firmados no se han alterado.</span><span class="sxs-lookup"><span data-stu-id="8942e-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="8942e-119">Genera dos números aleatorios de 32 bits criptográficamente seguros.</span><span class="sxs-lookup"><span data-stu-id="8942e-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="8942e-120">El primero es un número de secuencia de estado y el segundo es un número de secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="8942e-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="8942e-121">Cada vez que la aplicación envía un comando o una solicitud de estado, incrementa el número de secuencia correspondiente e incluye este número en el comando COPP o en los datos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8942e-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="8942e-122">Concatene el número aleatorio de 128 bits del controlador de gráficos, la clave de sesión AES, el número de secuencia de estado y el número de secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="8942e-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="8942e-123">Cifre esta matriz de bytes mediante la clave pública del controlador y pase el resultado a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="8942e-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="8942e-124">**Enviar comandos COPP y solicitudes de estado**</span><span class="sxs-lookup"><span data-stu-id="8942e-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="8942e-125">Consulte los tipos de protección disponibles y otra información mediante una llamada a [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span><span class="sxs-lookup"><span data-stu-id="8942e-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="8942e-126">Establezca los niveles de protección deseados llamando a [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span><span class="sxs-lookup"><span data-stu-id="8942e-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="8942e-127">Consulta periódicamente el nivel de protección local actual.</span><span class="sxs-lookup"><span data-stu-id="8942e-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="8942e-128">Detener la reproducción si el nivel de protección local cambia de forma inesperada o si se detecta un problema.</span><span class="sxs-lookup"><span data-stu-id="8942e-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8942e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8942e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8942e-130">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="8942e-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



