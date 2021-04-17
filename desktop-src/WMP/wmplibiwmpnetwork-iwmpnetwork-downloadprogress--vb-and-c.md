---
title: Propiedad downloadProgress de IWMPNetwork
description: La propiedad downloadProgress obtiene el porcentaje de descarga completada.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- propiedades de downloadProgress Media Player de Windows
- propiedad downloadProgress de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698572"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="84301-106">IWMPNetwork::d propiedad ownloadProgress</span><span class="sxs-lookup"><span data-stu-id="84301-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="84301-107">La propiedad **downloadProgress** obtiene el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="84301-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="84301-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84301-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="84301-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="84301-109">Property value</span></span>

<span data-ttu-id="84301-110">**System. Int32** que es el progreso de la descarga expresado como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="84301-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="84301-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84301-111">Remarks</span></span>

<span data-ttu-id="84301-112">Cuando el control de Media Player de Windows se conecta a un archivo multimedia digital que se puede reproducir y descargar al mismo tiempo, la propiedad **downloadProgress** obtiene el porcentaje del archivo total que se ha descargado.</span><span class="sxs-lookup"><span data-stu-id="84301-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="84301-113">Esta característica solo se admite actualmente para archivos multimedia digitales descargados de servidores Web.</span><span class="sxs-lookup"><span data-stu-id="84301-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="84301-114">Se puede descargar y reproducir simultáneamente un archivo con cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="84301-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="84301-115">Formato ASF</span><span class="sxs-lookup"><span data-stu-id="84301-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="84301-116">Audio de Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="84301-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="84301-117">Vídeo de Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="84301-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="84301-118">MP3</span><span class="sxs-lookup"><span data-stu-id="84301-118">MP3</span></span>
-   <span data-ttu-id="84301-119">MPEG</span><span class="sxs-lookup"><span data-stu-id="84301-119">MPEG</span></span>
-   <span data-ttu-id="84301-120">WAV</span><span class="sxs-lookup"><span data-stu-id="84301-120">WAV</span></span>

<span data-ttu-id="84301-121">Además, algunos archivos AVI se pueden descargar y reproducir simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="84301-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="84301-122">Use **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar cuándo se inicia o se detiene el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="84301-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="84301-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84301-123">Examples</span></span>

<span data-ttu-id="84301-124">En el ejemplo de código siguiente se usa **downloadProgress** para mostrar el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="84301-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="84301-125">La información se muestra en una etiqueta, en respuesta al evento de **almacenamiento en búfer** .</span><span class="sxs-lookup"><span data-stu-id="84301-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="84301-126">En el ejemplo se usa un temporizador con un intervalo de 1 segundo para actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="84301-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="84301-127">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="84301-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="84301-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84301-128">Requirements</span></span>



| <span data-ttu-id="84301-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="84301-129">Requirement</span></span> | <span data-ttu-id="84301-130">Value</span><span class="sxs-lookup"><span data-stu-id="84301-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84301-131">Versión</span><span class="sxs-lookup"><span data-stu-id="84301-131">Version</span></span><br/>   | <span data-ttu-id="84301-132">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="84301-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="84301-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84301-133">Namespace</span></span><br/> | <span data-ttu-id="84301-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="84301-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="84301-135">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="84301-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="84301-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="84301-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84301-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="84301-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84301-138">**Evento AxWindowsMediaPlayer. buffering (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="84301-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="84301-139">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="84301-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





