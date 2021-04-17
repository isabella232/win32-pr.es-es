---
title: Propiedad currentPosition de IWMPControls
description: La propiedad currentPosition obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- propiedades de currentPosition Media Player de Windows
- propiedad currentPosition de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690888"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="ab4f2-106">IWMPControls:: currentPosition (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ab4f2-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="ab4f2-107">La propiedad **currentPosition** obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.</span><span class="sxs-lookup"><span data-stu-id="ab4f2-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab4f2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab4f2-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="ab4f2-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ab4f2-109">Property value</span></span>

<span data-ttu-id="ab4f2-110">**System. Double** que es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="ab4f2-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="ab4f2-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ab4f2-111">Examples</span></span>

<span data-ttu-id="ab4f2-112">En el ejemplo siguiente se usa **currentPosition** para buscar una posición proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ab4f2-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="ab4f2-113">En respuesta a un clic de botón, **currentPosition** se establece en el valor especificado en un cuadro de texto denominado NewPosition.</span><span class="sxs-lookup"><span data-stu-id="ab4f2-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="ab4f2-114">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="ab4f2-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ab4f2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab4f2-115">Requirements</span></span>



| <span data-ttu-id="ab4f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab4f2-116">Requirement</span></span> | <span data-ttu-id="ab4f2-117">Value</span><span class="sxs-lookup"><span data-stu-id="ab4f2-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4f2-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ab4f2-118">Version</span></span><br/>   | <span data-ttu-id="ab4f2-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ab4f2-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ab4f2-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab4f2-120">Namespace</span></span><br/> | <span data-ttu-id="ab4f2-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ab4f2-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ab4f2-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ab4f2-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ab4f2-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ab4f2-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab4f2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab4f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4f2-125">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ab4f2-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ab4f2-126">**IWMPControls. currentPositionString (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ab4f2-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





