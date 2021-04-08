---
title: Para descodificar el audio a S/PDIF
description: Para descodificar el audio a S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- SDK de Windows Media Format, descodificación de audio a S/PDIF
- Windows Media Format SDK, formato de interconexión digital de Sony/Philips (S/PDIF)
- Advanced Systems Format (ASF), descodificar audio para S/PDIF
- ASF (formato de sistemas avanzados), descodificación de audio a S/PDIF
- Formato de sistemas avanzados (ASF), formato de interconexión digital de Sony/Philips (S/PDIF)
- ASF (formato de sistemas avanzados), formato de interconexión digital de Sony/Philips (S/PDIF)
- Formato de interconexión digital de Sony/Philips (S/PDIF), descodificación de audio
- S/PDIF (formato Sony/Philips digital Interconnect), descodificar audio
- descodificación de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789225"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="afd47-112">Para descodificar el audio a S/PDIF</span><span class="sxs-lookup"><span data-stu-id="afd47-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="afd47-113">El audio codificado con el códec Windows Media Audio 9 Professional se puede descodificar en formato de interconexión digital de Sony/Philips (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="afd47-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="afd47-114">Para generar la salida S/PDIF, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="afd47-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="afd47-115">Abra un archivo que contenga una secuencia Windows Media Audio 9 Professional llamando al método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="afd47-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="afd47-116">Identifique el número de salida de la secuencia que desee.</span><span class="sxs-lookup"><span data-stu-id="afd47-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="afd47-117">Para obtener más información, consulte [para identificar los números de salida](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="afd47-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="afd47-118">Llame al método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar la salida S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="afd47-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="afd47-119">Use g \_ wszEnableWMAProSPDIFOutput para el nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="afd47-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="afd47-120">El tipo de datos es el **\_ tipo WMT \_ bool**; establezca el valor en **true** para habilitar la salida S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="afd47-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="afd47-121">Obtenga la interfaz de propiedades de salida ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) del formato de salida deseado llamando al método [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) .</span><span class="sxs-lookup"><span data-stu-id="afd47-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="afd47-122">Para obtener más información sobre cómo enumerar los formatos de salida, vea [asignar formatos de salida](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="afd47-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="afd47-123">Establezca el formato de salida llamando al método [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) .</span><span class="sxs-lookup"><span data-stu-id="afd47-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="afd47-124">Pase un puntero a la interfaz **IWMOutputMediaProps** obtenida en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="afd47-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="afd47-125">Realice cualquier otro cambio de configuración y comience la reproducción.</span><span class="sxs-lookup"><span data-stu-id="afd47-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="afd47-126">Puede realizar los pasos anteriores en el lector sincrónico mediante los métodos correspondientes de la interfaz [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="afd47-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="afd47-127">En el ejemplo de código siguiente se muestra cómo establecer una secuencia de audio para generar audio como datos S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="afd47-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="afd47-128">Esta función supone que ya se ha cargado un archivo en el lector y que se ha identificado el número de salida.</span><span class="sxs-lookup"><span data-stu-id="afd47-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="afd47-129">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="afd47-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="afd47-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="afd47-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afd47-131">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="afd47-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="afd47-132">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="afd47-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="afd47-133">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="afd47-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="afd47-134">**Interfaz IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="afd47-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="afd47-135">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="afd47-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




