---
description: En el modelo de canalización de bases de medios, un origen multimedia se conecta a una transformación que se conecta aún más a un receptor de medios.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componentes ASF de capa de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715511"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="15eea-103">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="15eea-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="15eea-104">En el modelo de canalización de Media Foundation, un origen multimedia se conecta a una transformación que se conecta aún más a un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="15eea-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="15eea-105">Los datos contenidos en el origen fluyen a través de la transformación y generan ejemplos de medios de salida en el receptor con el fin de reproducir o codificar.</span><span class="sxs-lookup"><span data-stu-id="15eea-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="15eea-106">En función de si la aplicación desea reproducir contenido ASF o codificar en un archivo ASF, la aplicación debe compilar la canalización de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="15eea-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="15eea-107">Los temas siguientes contienen información sobre los componentes de la capa de canalización.</span><span class="sxs-lookup"><span data-stu-id="15eea-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="15eea-108">Origen de medios ASF</span><span class="sxs-lookup"><span data-stu-id="15eea-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="15eea-109">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="15eea-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="15eea-110">Receptores de medios ASF</span><span class="sxs-lookup"><span data-stu-id="15eea-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="15eea-111">Los tres componentes principales de una canalización ASF para la reproducción son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="15eea-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="15eea-112">El origen de medios ASF lo proporciona Media Foundation que representa un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="15eea-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="15eea-113">Remuestreadores de audio, cambiar el tamaño de las imágenes de vídeo, etc., (transformación)</span><span class="sxs-lookup"><span data-stu-id="15eea-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="15eea-114">Representador de audio y vídeo (receptores)</span><span class="sxs-lookup"><span data-stu-id="15eea-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="15eea-115">Para obtener información sobre la creación de una canalización de reproducción, vea [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="15eea-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="15eea-116">Los tres componentes principales de una canalización ASF para la codificación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="15eea-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="15eea-117">Origen multimedia que representa los datos en un formato que debe convertirse.</span><span class="sxs-lookup"><span data-stu-id="15eea-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="15eea-118">Este componente puede ser uno de los orígenes de medios predeterminados proporcionados por Media Foundation o un origen personalizado que exponga la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="15eea-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="15eea-119">Codificadores de Windows Media (transformación) que realizan la conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="15eea-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="15eea-120">Receptores de medios ASF proporcionados por Media Foundation que escriben objetos ASF y ejemplos de medios en un archivo de salida especificado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15eea-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="15eea-121">La canalización se representa en una topología y cada objeto de la canalización se representa mediante un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="15eea-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="15eea-122">Tanto para la reproducción como para la codificación, la sesión multimedia controla todas las operaciones de canalización.</span><span class="sxs-lookup"><span data-stu-id="15eea-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="15eea-123">Una de las responsabilidades de la sesión multimedia es asegurarse de que la canalización tenga todos los componentes necesarios para generar la salida.</span><span class="sxs-lookup"><span data-stu-id="15eea-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="15eea-124">Por ejemplo, en una canalización de codificación, si el formato de origen de audio es diferente del formato de destino, la sesión multimedia inserta componentes de transformación adicionales, como el remuestreador que realiza las conversiones de velocidad de muestra apropiadas.</span><span class="sxs-lookup"><span data-stu-id="15eea-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="15eea-125">La sesión multimedia también administra el control de flujo de datos a través de la canalización.</span><span class="sxs-lookup"><span data-stu-id="15eea-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="15eea-126">En un escenario de reproducción, al iniciar la sesión multimedia, la sesión multimedia envía muestras a SAR y EVR, que las representa en el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="15eea-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="15eea-127">Para la codificación, el inicio de la sesión multimedia inicia el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="15eea-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="15eea-128">La sesión notifica de forma asincrónica a la aplicación cuando se completa la codificación.</span><span class="sxs-lookup"><span data-stu-id="15eea-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="15eea-129">El siguiente tema contiene instrucciones paso a paso sobre el uso de los componentes de la capa de canalización para crear una topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="15eea-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="15eea-130">componentes para leer y escribir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="15eea-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="15eea-131">Tutorial: 1-pasar la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="15eea-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="15eea-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15eea-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15eea-133">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15eea-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



