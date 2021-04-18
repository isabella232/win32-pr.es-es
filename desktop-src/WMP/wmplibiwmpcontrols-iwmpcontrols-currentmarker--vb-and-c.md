---
title: Propiedad currentMarker de IWMPControls
description: La propiedad currentMarker obtiene o establece el número de marcador actual.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- propiedades de currentMarker Media Player de Windows
- propiedad currentMarker de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690890"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="2a497-106">IWMPControls:: currentMarker (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2a497-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="2a497-107">La propiedad **currentMarker** obtiene o establece el número de marcador actual.</span><span class="sxs-lookup"><span data-stu-id="2a497-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a497-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a497-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2a497-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2a497-109">Property value</span></span>

<span data-ttu-id="2a497-110">**System. Int32** que es el número del marcador.</span><span class="sxs-lookup"><span data-stu-id="2a497-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a497-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a497-111">Remarks</span></span>

<span data-ttu-id="2a497-112">La configuración de **currentMarker** hace que la reproducción se inicie desde el marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="2a497-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="2a497-113">Antes de intentar establecer **currentMarker**, determine si un archivo tiene marcadores y cuántos tiene con **IWMPMedia. markerCount**.</span><span class="sxs-lookup"><span data-stu-id="2a497-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="2a497-114">Si un archivo no tiene marcadores, si se establece **currentMarker** en cualquier cosa pero cero, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a497-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="2a497-115">Establecer **currentMarker** en un número mayor que **markerCount** también produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a497-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="2a497-116">La propiedad **currentMarker** siempre devuelve el marcador actual o el último, lo que significa que la posición del archivo real puede estar en el marcador actual o antes del marcador siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a497-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="2a497-117">Los marcadores se numeran a partir de 1, por lo que si un archivo tiene marcadores, puede establecer **currentMarker** en cero para cambiar la posición del archivo a cero.</span><span class="sxs-lookup"><span data-stu-id="2a497-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="2a497-118">Hasta que se establezca el elemento multimedia actual (mediante **AxWindowsMediaPlayer. URL** o **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2a497-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="2a497-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2a497-119">Examples</span></span>

<span data-ttu-id="2a497-120">En el ejemplo siguiente se usa **currentMarker** para iniciar la reproducción de vídeo desde el marcador que corresponde a la propiedad SelectedIndex de un cuadro de lista que se ha rellenado con identificadores de marcador.</span><span class="sxs-lookup"><span data-stu-id="2a497-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="2a497-121">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="2a497-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2a497-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a497-122">Requirements</span></span>



| <span data-ttu-id="2a497-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a497-123">Requirement</span></span> | <span data-ttu-id="2a497-124">Value</span><span class="sxs-lookup"><span data-stu-id="2a497-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a497-125">Versión</span><span class="sxs-lookup"><span data-stu-id="2a497-125">Version</span></span><br/>   | <span data-ttu-id="2a497-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2a497-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2a497-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a497-127">Namespace</span></span><br/> | <span data-ttu-id="2a497-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2a497-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2a497-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2a497-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2a497-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2a497-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a497-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a497-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a497-132">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2a497-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a497-133">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2a497-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a497-134">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2a497-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a497-135">**IWMPMedia. markerCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2a497-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





