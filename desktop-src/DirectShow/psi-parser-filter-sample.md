---
description: Ejemplo de filtro de analizador de PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Ejemplo de filtro de analizador de PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552732"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="02156-103">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="02156-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="02156-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="02156-104">Description</span></span>

<span data-ttu-id="02156-105">El filtro del analizador de PSI recibe información específica del programa (PSI) de una secuencia de transporte MPEG-2 y extrae información del programa de la tabla de Asociación de programas (PAT) y de las tablas de mapa de programa (PMT).</span><span class="sxs-lookup"><span data-stu-id="02156-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="02156-106">Esta información permite a una aplicación configurar el desmultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="02156-107">El filtro admite una interfaz personalizada, [**IMpeg2PsiParser**](impeg2psiparser.md), para recuperar la información de PSI.</span><span class="sxs-lookup"><span data-stu-id="02156-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="02156-108">Este filtro está diseñado para dispositivos MPEG-2, como camascopios IEEE 1394 MPEG-2 y dispositivos D-VHS.</span><span class="sxs-lookup"><span data-stu-id="02156-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="02156-109">Consulte [controlador MSTape](mstape-driver.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="02156-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="02156-110">Los orígenes de difusión de televisión digital deben usar un filtro TIF para obtener información del programa.</span><span class="sxs-lookup"><span data-stu-id="02156-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="02156-111">Uso</span><span class="sxs-lookup"><span data-stu-id="02156-111">Usage</span></span>

<span data-ttu-id="02156-112">Puede probar el filtro del analizador de PSI en GraphEdit como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="02156-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="02156-113">Inicie GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="02156-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="02156-114">Inserte un origen de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="02156-115">Las videocámaras MPEG-2 y los dispositivos D-VHS aparecen como "dispositivo de subunidad de cinta AV/C de Microsoft" en la categoría de orígenes de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02156-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="02156-116">Conecte el filtro de origen al filtro de demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="02156-117">Use la página de propiedades de Demux para crear un PIN de salida con un tipo de medio "MPEG-2 PSI".</span><span class="sxs-lookup"><span data-stu-id="02156-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="02156-118">Este pin proporcionará las secciones PAT y PMT.</span><span class="sxs-lookup"><span data-stu-id="02156-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="02156-119">Use la página de propiedades Demux para asignar el PID 0x00 al terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="02156-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="02156-120">Establezca el tipo de contenido en "secciones de PSI de MPEG2".</span><span class="sxs-lookup"><span data-stu-id="02156-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="02156-121">Conecte el PIN de salida de Demux al analizador de PSI, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="02156-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![gráfico de filtro del analizador de PSI](images/psi-parser.png)

7.  <span data-ttu-id="02156-123">Ejecute el gráfico para alimentar los datos de la PSI al filtro del analizador de PSI.</span><span class="sxs-lookup"><span data-stu-id="02156-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="02156-124">A medida que el filtro descodifica las secciones PAT, asigna automáticamente los PID de pago al mismo pin de salida en el Demux, de modo que recibe las secciones PMT.</span><span class="sxs-lookup"><span data-stu-id="02156-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="02156-125">Use la página de propiedades del analizador de PSI para seleccionar un número de programa.</span><span class="sxs-lookup"><span data-stu-id="02156-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="02156-126">La lista de secuencias elementales de la página de propiedades mostrará el PID y el tipo de secuencia asociados a cada flujo elemental en el programa seleccionado.</span><span class="sxs-lookup"><span data-stu-id="02156-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="02156-127">La página de propiedades está diseñada para reconocer los tipos de secuencia definidos en ISO/IEC 13818-1.</span><span class="sxs-lookup"><span data-stu-id="02156-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="02156-128">Escriba el número de PID de audio en el cuadro de edición **PID de audio** y el número de PID de vídeo en el cuadro de edición **PID de vídeo** .</span><span class="sxs-lookup"><span data-stu-id="02156-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="02156-129">Haga clic en el botón **Ver programa** .</span><span class="sxs-lookup"><span data-stu-id="02156-129">Click the **View Program** button.</span></span> <span data-ttu-id="02156-130">El analizador de PSI configurará los pin de salida en Demux para que coincidan con la información de la secuencia de programa y representen los pin.</span><span class="sxs-lookup"><span data-stu-id="02156-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="02156-131">La página de propiedades del analizador de PSI se proporciona para facilitar la realización de pruebas y proporcionar código de ejemplo que configura el desmultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="02156-132">No se recomienda para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="02156-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="02156-133">Las aplicaciones deben configurar el Demux mediante programación.</span><span class="sxs-lookup"><span data-stu-id="02156-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="02156-134">Para usar el filtro del analizador PSI en una aplicación, empiece por crear el gráfico de filtros desde el origen MPEG-2 hasta el Demux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="02156-135">Aquí no se muestra el código de este paso, ya que la configuración exacta del gráfico dependerá del origen.</span><span class="sxs-lookup"><span data-stu-id="02156-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="02156-136">A continuación, cree un PIN de salida en Demux para los datos de PSI.</span><span class="sxs-lookup"><span data-stu-id="02156-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="02156-137">Asigne el PID 0x00, que está reservado para las secciones PAT, a este pin, como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="02156-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="02156-138">Para obtener más información, consulte [uso del demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="02156-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="02156-139">Agregue el filtro de analizador de PSI al gráfico y conéctelo al pin de salida en el Demux.</span><span class="sxs-lookup"><span data-stu-id="02156-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="02156-140">Consulte el analizador de PSI para la interfaz [**IMpeg2PsiParser**](impeg2psiparser.md) .</span><span class="sxs-lookup"><span data-stu-id="02156-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="02156-141">Ahora ejecute el gráfico y espere a \_ que se \_ hayan cambiado los eventos del programa EC, que señalan una nueva sección Pat o PMT.</span><span class="sxs-lookup"><span data-stu-id="02156-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="02156-142">Este evento es un evento personalizado definido por el filtro del analizador PSI.</span><span class="sxs-lookup"><span data-stu-id="02156-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="02156-143">Cuando reciba un evento de \_ cambio de programa de EC \_ , puede obtener la información de PSI disponible llamando a métodos **IMpeg2PsiParser** .</span><span class="sxs-lookup"><span data-stu-id="02156-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="02156-144">En esta sección se describen los métodos que necesitará con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="02156-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="02156-145">Para obtener el número de programas, use el método [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :</span><span class="sxs-lookup"><span data-stu-id="02156-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="02156-146">Para obtener el número de programa para un programa específico, use el método [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :</span><span class="sxs-lookup"><span data-stu-id="02156-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="02156-147">El número de programa se usa para obtener las entradas de pago de programas individuales.</span><span class="sxs-lookup"><span data-stu-id="02156-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="02156-148">Para obtener el número de flujos elementales en un programa, use el método [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :</span><span class="sxs-lookup"><span data-stu-id="02156-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="02156-149">Para cada flujo elemental, el método [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) devuelve el PID y el método [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) devuelve el tipo de flujo:</span><span class="sxs-lookup"><span data-stu-id="02156-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="02156-150">El PID y el tipo de secuencia permiten configurar nuevas clavijas de salida en el demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="02156-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="02156-151">Esto puede requerir cierto conocimiento del origen original.</span><span class="sxs-lookup"><span data-stu-id="02156-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="02156-152">Por ejemplo, ISO/IEC 13818-1 define tipos de secuencia de 0x80 a 0xFF como "usuario privado", pero otros estándares basados en MPEG-2 pueden asignar otros significados a estos tipos.</span><span class="sxs-lookup"><span data-stu-id="02156-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="02156-153">El demultiplexador MPEG-2 puede crear nuevos PIN y nuevas asignaciones de PID mientras el gráfico se está ejecutando, pero debe detener el gráfico para conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="02156-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="02156-154">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02156-154">Downloading the Sample</span></span>

<span data-ttu-id="02156-155">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="02156-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="02156-156">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ PSIParser.</span><span class="sxs-lookup"><span data-stu-id="02156-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02156-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02156-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02156-158">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="02156-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="02156-159">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="02156-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
