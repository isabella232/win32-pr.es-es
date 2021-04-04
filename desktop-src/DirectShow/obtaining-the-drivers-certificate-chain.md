---
description: Obtención de la cadena de certificados de los controladores
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtención de la cadena de certificados de los controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906331"
---
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="4cb7d-103">Obtención de la cadena de certificados de los controladores</span><span class="sxs-lookup"><span data-stu-id="4cb7d-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="4cb7d-104">Para usar el protocolo de protección de la salida certificada (COPP), la aplicación debe crear primero un grafo de DirectShow que incluya el filtro de representación de combinación de vídeo (VMR-7 o VMR-9).</span><span class="sxs-lookup"><span data-stu-id="4cb7d-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="4cb7d-105">El filtro de representador de vídeo anterior no es compatible con COPP.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="4cb7d-106">Antes de llamar a cualquier método COPP, la aplicación debe crear un gráfico de reproducción de vídeo y conectar el descodificador al pin de entrada del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="4cb7d-107">No es necesario reproducir el archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="4cb7d-108">Después de compilar el gráfico, consulte VMR para la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) y, a continuación, llame a [**IAMCertifiedOutputProtection:: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="4cb7d-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="4cb7d-109">Este método devuelve un número aleatorio de 128 bits con tipo como GUID, junto con un puntero a una matriz de bytes que contiene la cadena de certificados XML del controlador en formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="4cb7d-110">En el código siguiente se muestra cómo obtener la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="4cb7d-110">The following code shows how to get the certificate chain.</span></span>


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a><span data-ttu-id="4cb7d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb7d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cb7d-112">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="4cb7d-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



