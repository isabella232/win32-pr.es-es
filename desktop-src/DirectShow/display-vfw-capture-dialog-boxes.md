---
description: Mostrar cuadros de diálogo de captura de VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Mostrar cuadros de diálogo de captura de VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805389"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="7355b-103">Mostrar cuadros de diálogo de captura de VFW</span><span class="sxs-lookup"><span data-stu-id="7355b-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="7355b-104">Un dispositivo de captura que todavía usa un controlador de vídeo para Windows (VFW) puede admitir cualquiera de los tres cuadros de diálogo siguientes, que se usan para configurar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7355b-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="7355b-105">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="7355b-105">Dialog box</span></span>    | <span data-ttu-id="7355b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7355b-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7355b-107">Origen de vídeo</span><span class="sxs-lookup"><span data-stu-id="7355b-107">Video Source</span></span>  | <span data-ttu-id="7355b-108">Se usa para seleccionar la entrada de vídeo y para ajustar la configuración del dispositivo, como el brillo o el contraste de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7355b-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="7355b-109">Formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="7355b-109">Video Format</span></span>  | <span data-ttu-id="7355b-110">Se usa para seleccionar las dimensiones de la imagen y la profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="7355b-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="7355b-111">Pantalla de vídeo</span><span class="sxs-lookup"><span data-stu-id="7355b-111">Video Display</span></span> | <span data-ttu-id="7355b-112">Se usa para controlar la apariencia del vídeo representado.</span><span class="sxs-lookup"><span data-stu-id="7355b-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="7355b-113">Para mostrar uno de estos cuadros de diálogo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7355b-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="7355b-114">Detenga el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7355b-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="7355b-115">Consulte el filtro de captura para la interfaz [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) .</span><span class="sxs-lookup"><span data-stu-id="7355b-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="7355b-116">Si **QueryInterface** se realiza correctamente, significa que el dispositivo de captura es un dispositivo VFW.</span><span class="sxs-lookup"><span data-stu-id="7355b-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="7355b-117">Llame a [**IAMVfwCaptureDialogs:: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) para comprobar si el controlador admite el cuadro de diálogo que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="7355b-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="7355b-118">La enumeración [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) define marcas para cada uno de los cuadros de diálogo VFW.</span><span class="sxs-lookup"><span data-stu-id="7355b-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="7355b-119">**HasDialog** devuelve S \_ OK si se admite el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7355b-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="7355b-120">Devuelve S \_ false en caso contrario, por lo que debe comprobar el valor s \_ OK directamente, en lugar de usar la macro **Succeeded** .</span><span class="sxs-lookup"><span data-stu-id="7355b-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="7355b-121">Si se admite el cuadro de diálogo, llame a [**IAMVfwCaptureDialogs:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) para mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7355b-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="7355b-122">Reinicie el gráfico.</span><span class="sxs-lookup"><span data-stu-id="7355b-122">Restart the graph.</span></span>

<span data-ttu-id="7355b-123">En el código siguiente se muestran estos pasos para el cuadro de diálogo origen de vídeo:</span><span class="sxs-lookup"><span data-stu-id="7355b-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="7355b-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7355b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7355b-125">Configuración de un dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7355b-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



