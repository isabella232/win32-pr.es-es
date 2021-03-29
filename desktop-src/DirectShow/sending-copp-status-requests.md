---
description: Envío de solicitudes de estado de COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Envío de solicitudes de estado de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805210"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="2adef-103">Envío de solicitudes de estado de COPP</span><span class="sxs-lookup"><span data-stu-id="2adef-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="2adef-104">Para enviar una solicitud de estado del Protocolo de protección de la salida (COPP), rellene una estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) con los datos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2adef-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="2adef-105">Los miembros de la estructura son:</span><span class="sxs-lookup"><span data-stu-id="2adef-105">The structure members are:</span></span>

-   <span data-ttu-id="2adef-106">**rApp**.</span><span class="sxs-lookup"><span data-stu-id="2adef-106">**rApp**.</span></span> <span data-ttu-id="2adef-107">Número aleatorio de 128 bits, escrito como un GUID.</span><span class="sxs-lookup"><span data-stu-id="2adef-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="2adef-108">Se devuelve el mismo número en la respuesta del controlador.</span><span class="sxs-lookup"><span data-stu-id="2adef-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="2adef-109">Debe asignar el número aleatorio en el montón y, a continuación, copiarlo en la estructura.</span><span class="sxs-lookup"><span data-stu-id="2adef-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="2adef-110">Esto protege contra los ataques en los que el atacante modifica el contenido de la estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .</span><span class="sxs-lookup"><span data-stu-id="2adef-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="2adef-111">**guidStatusRequestID**.</span><span class="sxs-lookup"><span data-stu-id="2adef-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="2adef-112">GUID que identifica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2adef-112">A GUID that identifies the request.</span></span> <span data-ttu-id="2adef-113">Consulte [referencia de consulta de COPP](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2adef-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="2adef-114">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="2adef-114">**dwSequence**.</span></span> <span data-ttu-id="2adef-115">El número de secuencia de estado.</span><span class="sxs-lookup"><span data-stu-id="2adef-115">The status sequence number.</span></span> <span data-ttu-id="2adef-116">Incremente este valor después de cada solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="2adef-116">Increment this value after each status request.</span></span> <span data-ttu-id="2adef-117">(En la sección [Inicio de una sesión de COPP](initiating-a-copp-session.md), este valor se muestra como *uStatusSeq* en los ejemplos de código).</span><span class="sxs-lookup"><span data-stu-id="2adef-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="2adef-118">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="2adef-118">**cbSizeData**.</span></span> <span data-ttu-id="2adef-119">Tamaño, en bytes, de los datos adicionales necesarios para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2adef-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="2adef-120">**StatusData**.</span><span class="sxs-lookup"><span data-stu-id="2adef-120">**StatusData**.</span></span> <span data-ttu-id="2adef-121">Datos de la solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="2adef-121">Data for the status request.</span></span>

<span data-ttu-id="2adef-122">Pase la estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) al método [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) .</span><span class="sxs-lookup"><span data-stu-id="2adef-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="2adef-123">Por ejemplo, el código siguiente envía una solicitud de estado que consulta qué mecanismos de protección están disponibles:</span><span class="sxs-lookup"><span data-stu-id="2adef-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="2adef-124">La respuesta se escribe en el miembro **COPPStatus** de la estructura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) .</span><span class="sxs-lookup"><span data-stu-id="2adef-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="2adef-125">El tamaño de los datos válidos en la respuesta se proporciona en el miembro **cbSizeData** .</span><span class="sxs-lookup"><span data-stu-id="2adef-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="2adef-126">Para garantizar la integridad del mensaje, el controlador calcula un código de autenticación de mensajes (MAC) mediante el algoritmo OMAC 1 y devuelve este valor en el miembro **macKDI** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="2adef-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="2adef-127">La aplicación debe comprobar este valor de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2adef-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="2adef-128">Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **macKDI** de la estructura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (es decir, **cbSizeData** más **COPPStatus**).</span><span class="sxs-lookup"><span data-stu-id="2adef-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="2adef-129">Compare esta etiqueta con el valor de **macKDI**, con un **memcmp** recto.</span><span class="sxs-lookup"><span data-stu-id="2adef-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="2adef-130">El algoritmo OMAC 1 se describe en detalle en [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="2adef-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="2adef-131">COPP usa los siguientes parámetros de OMAC-1:</span><span class="sxs-lookup"><span data-stu-id="2adef-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="2adef-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="2adef-132">E = AES</span></span>
-   <span data-ttu-id="2adef-133">t = 128 bits</span><span class="sxs-lookup"><span data-stu-id="2adef-133">t = 128 bits</span></span>

<span data-ttu-id="2adef-134">Los datos devueltos por la solicitud de estado siempre comienzan con dos elementos:</span><span class="sxs-lookup"><span data-stu-id="2adef-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="2adef-135">El mismo valor de **rApp** pasado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2adef-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="2adef-136">Debe comprobar que este valor coincide con el valor original almacenado en el montón.</span><span class="sxs-lookup"><span data-stu-id="2adef-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="2adef-137">Un valor de [**COPP \_ StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) que indica si el estado de protección de salida ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2adef-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="2adef-138">Dado que se puede perder o volver a configurar la conexión, la aplicación debe sondear periódicamente el estado actual del controlador.</span><span class="sxs-lookup"><span data-stu-id="2adef-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="2adef-139">Si \_ se establece la marca RenegotiationRequired de COPP, la aplicación debe intentar restablecer el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="2adef-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="2adef-140">Si \_ se establece la marca LinkLost de COPP, la aplicación debe detener la reproducción del contenido.</span><span class="sxs-lookup"><span data-stu-id="2adef-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="2adef-141">Por ejemplo, \_ se puede devolver la marca LinkLost de COPP porque el usuario desconectó el conector de salida.</span><span class="sxs-lookup"><span data-stu-id="2adef-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="2adef-142">La aplicación debe liberar la instancia actual de VMR, crear una nueva instancia de VMR y establecer una nueva sesión de COPP (incluido el intercambio de claves y la validación de certificados).</span><span class="sxs-lookup"><span data-stu-id="2adef-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2adef-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2adef-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2adef-144">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="2adef-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



