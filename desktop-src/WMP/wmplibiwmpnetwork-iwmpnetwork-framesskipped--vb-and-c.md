---
title: Propiedad framesSkipped de IWMPNetwork
description: La propiedad framesSkipped obtiene el número total de fotogramas omitidos durante la reproducción.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- propiedades de framesSkipped Media Player de Windows
- propiedad framesSkipped de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670885"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="e8e4f-106">IWMPNetwork:: framesSkipped (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e8e4f-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="e8e4f-107">La propiedad **framesSkipped** obtiene el número total de fotogramas omitidos durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e4f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e4f-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e8e4f-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8e4f-109">Property value</span></span>

<span data-ttu-id="e8e4f-110">**System. Int32** que es el número de fotogramas omitidos.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="e8e4f-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8e4f-111">Examples</span></span>

<span data-ttu-id="e8e4f-112">En el ejemplo de código siguiente se usa **framesSkipped** para mostrar el número total de fotogramas omitidos durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="e8e4f-113">La información se muestra en una etiqueta cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="e8e4f-114">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="e8e4f-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e8e4f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e4f-115">Requirements</span></span>



| <span data-ttu-id="e8e4f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e4f-116">Requirement</span></span> | <span data-ttu-id="e8e4f-117">Value</span><span class="sxs-lookup"><span data-stu-id="e8e4f-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e4f-118">Versión</span><span class="sxs-lookup"><span data-stu-id="e8e4f-118">Version</span></span><br/>   | <span data-ttu-id="e8e4f-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e8e4f-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e8e4f-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8e4f-120">Namespace</span></span><br/> | <span data-ttu-id="e8e4f-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e8e4f-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e8e4f-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e8e4f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e8e4f-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e4f-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e4f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e4f-125">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e8e4f-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





