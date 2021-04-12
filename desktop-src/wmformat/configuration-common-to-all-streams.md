---
title: Configuración común para todos los flujos
description: Configuración común para todos los flujos
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- perfiles, configuraciones comunes a todos los flujos
- flujos, configuraciones comunes
- flujos, nombres
- flujos, nombres de conexión
- secuencias, números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104420475"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="2cf52-108">Configuración común para todos los flujos</span><span class="sxs-lookup"><span data-stu-id="2cf52-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="2cf52-109">A todas las secuencias, independientemente del tipo, se les debe asignar un nombre de flujo, un nombre de conexión y un número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="2cf52-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="2cf52-110">El nombre del flujo es simplemente un nombre descriptivo que se asigna a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2cf52-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="2cf52-111">No es necesario que una secuencia tenga un nombre de flujo, pero ayuda a identificar la secuencia al editar el perfil en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="2cf52-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="2cf52-112">Puede establecer un nombre para la secuencia mediante una llamada a [**IWMStreamConfig:: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span><span class="sxs-lookup"><span data-stu-id="2cf52-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="2cf52-113">Cada secuencia debe tener un nombre de conexión, también denominado nombre de entrada.</span><span class="sxs-lookup"><span data-stu-id="2cf52-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="2cf52-114">Al establecer el perfil en el objeto de escritor para escribir un archivo, el escritor asociará cada nombre de conexión con una entrada.</span><span class="sxs-lookup"><span data-stu-id="2cf52-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="2cf52-115">Para identificar las entradas, debe llamar a [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) para recuperar el nombre de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2cf52-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="2cf52-116">Los nombres de conexión típicos son descripciones simples del contenido, como "audio".</span><span class="sxs-lookup"><span data-stu-id="2cf52-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="2cf52-117">Si el perfil contiene secuencias que se excluyen mutuamente mediante la velocidad de bits, cada una de las secuencias mutuamente excluyentes debe tener el mismo nombre de conexión.</span><span class="sxs-lookup"><span data-stu-id="2cf52-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="2cf52-118">Si no es así, el perfil no es válido y el escritor lo rechazará.</span><span class="sxs-lookup"><span data-stu-id="2cf52-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="2cf52-119">Puede establecer un nombre de conexión llamando a [**IWMStreamConfig:: SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span><span class="sxs-lookup"><span data-stu-id="2cf52-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="2cf52-120">El número de secuencia identifica la secuencia dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="2cf52-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="2cf52-121">A diferencia de los números de entrada y de salida, los números de flujo comienzan en 1, no en 0.</span><span class="sxs-lookup"><span data-stu-id="2cf52-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="2cf52-122">Un número de secuencia es diferente de un índice de flujo, que se usa al obtener secuencias en un perfil mediante [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="2cf52-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="2cf52-123">El índice de la secuencia es un número asignado a la secuencia por el objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="2cf52-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="2cf52-124">Los índices de secuencia oscilan entre 0 y uno menos que el número de flujos recuperados por [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span><span class="sxs-lookup"><span data-stu-id="2cf52-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="2cf52-125">Los números de secuencia no deben ser secuenciales, aunque normalmente son, y pueden oscilar entre 1 y 63.</span><span class="sxs-lookup"><span data-stu-id="2cf52-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="2cf52-126">Puede establecer un número de secuencia mediante una llamada a [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span><span class="sxs-lookup"><span data-stu-id="2cf52-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cf52-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cf52-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf52-128">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="2cf52-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="2cf52-129">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="2cf52-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




